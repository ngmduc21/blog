---
title: "Xung đột giữa Hyper-V và WSL2?"
date: 2021-09-15
categories: System
---

Bài viết này giới thiệu công nghệ Hyper-V, WSL2 và cách giải quyết lỗi xung đột giữa chúng.
<!-- excerpt-end -->
# Hyper-V, VT-x, AMD-v và WSL2

Hyper-V là một nền tảng ảo hóa mạnh mẽ được tích hợp vào Windows, được sử dụng rộng rãi trong các công cụ dành cho developer như Docker và mới nhất là WSL2. Đi kèm và bổ trợ cho Hyper-V là công nghệ ảo hóa tích hợp đến từ Intel và AMD - VT-x và AMD-v. Hiện tại ta có thể sử dụng 2 engine này cho việc chạy máy ảo trên VMWare và cho hiệu suất ổn định hơn. 

WSL2 - Windows Subsystem for Linux là một tính năng có trên Windows 10 giúp cho phép chạy hệ điều hành Linux (GNU/Linux) trên Windows. Với WSL các nhà phát triển có thể chạy cách lệnh, các ứng dụng Linux ngay từ Windows Terminal (tích hợp Terminal từ các HĐH Linux con) mà không cần phải bận tâm về việc tạo hay quản lý các máy ảo như trước đây. WSL giúp các developers tối giản hóa các bước cài đặt môi trường và cung cấp một hiệu suất cao hơn.

# Kiểm tra và bật WSL2, Hyper-V, VT-x

## Bật WSL2 Hyper-V và VT-x

Hyper-V hiện có sẵn trên các phiên bản Windows 10 Pro, Windows 10 Home thì ta dùng câu lệnh này trong PowerShell (quyền Administrator) để bật:

```
DISM /Online /Enable-Feature /All /FeatureName:Microsoft-Hyper-V
```

Để bật Hyper-V, ta vào Control Panel → Programs → Turn Windows Features on or off → Check ở ô Hyper-V

![Untitled](/blog/assets/post03/Untitled.png)

Để bật VT-x ta vào BIOS (tùy các hãng sản xuất mà cách vào BIOS sẽ khác nhau) và tìm bật tùy chọn Intel® Virtualization Technology.

Ở WSL2 ta cần phải bật thêm những features sau:

- Virtual Machine Platform
- Windows Hypervisor Platform
- Windows Subsystem for Linux

![Untitled1](/blog/assets/post03/Untitled1.png)

Khi check xong và chờ máy restart, ta có thể bắt đầu lên Microsoft Store để download HĐH ta cần tích hợp và bắt đầu chạy. Chi tiết tham khảo tại [đây](https://docs.microsoft.com/en-us/windows/wsl/install-win10) 

## Kiểm tra Hyper-V, VT-x

Ta dùng 2 công cụ sau:

- [Intel® Processor Identification Utility](https://www.intel.com/content/www/us/en/support/articles/000005495.html) để kiểm tra hệ thống của chúng ta có hỗ trợ công nghệ VT-x hay không. Để ý 2 dòng sau:

![Untitled2](/blog/assets/post03/Untitled2.png)

- Task Manager của Windows: để ý thông số "Virtualization"

![Untitled3](/blog/assets/post03/Untitled3.png)

- So sánh trong bảng sau:

![tablesosanh](/blog/assets/post03/tablesosanh.png)

# Vấn đề xung đột

Bởi vì Hyper-V là một feature khá "tham lam", khi bật nó sẽ không cho phép bất kì tiến trình ảo hóa ngoài luồng chạy. Khi dùng Hyper-V chạy dưới hệ thống WSL2 sẽ xảy ra vấn đề với các phần mềm bên thứ 3 như VMWare hay VirtualBox - không thể sử dụng Hyper-V hay các engine VT-x để thực hiện ảo hóa. Ta chỉ có thể chọn 1 trong 2 như sau:

Vào Command Prompt dưới quyền Administrator và gõ:

```python
bcdedit /set hypervisorlaunchtype auto
```

Tùy chọn này ta sẽ bật HyperV sử dụng cho WSL2 và tắt với các phần mềm bên thứ 3 (VMWare). Mình đã thử thì tùy chọn này vẫn sẽ cho phép Docker Container chạy trên nền WSL2.

```python
bcdedit /set hypervisorlaunchtype off
```

Tùy chọn này ta sẽ tắt HyperV sử dụng cho WSL2 và bật với các phần mềm bên thứ 3 (VMWare).

Hy vọng bài viết của mình sẽ giúp mọi người tiết kiệm thời gian trong việc tìm cách khắc phục lỗi này.