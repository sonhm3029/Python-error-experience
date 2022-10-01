# Python-error-experience

# Table of contents

- [Python-error-experience](#python-error-experience)
  - [1. Lỗi `RuntimeError` khi chạy multiprocessing ngoài vòng `main`:](#1-li-runtimeerror-khi-chy-multiprocessing-ngoi-vng-main)

## 1. Lỗi `RuntimeError` khi chạy multiprocessing ngoài vòng `main`

Stackovervlow: [https://stackoverflow.com/questions/18204782/runtimeerror-on-windows-trying-python-multiprocessing](https://stackoverflow.com/questions/18204782/runtimeerror-on-windows-trying-python-multiprocessing)

**Nguyên nhân:** Do trên windows, `subprocesses` import main module khi chạy project => cần phải đặt các task multiprocessing vào trong `if __name__ == '__main__'.
