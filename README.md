# Trang web OptiVisionLab

[![Deploy Docs](https://github.com/optivisionlab/labs/actions/workflows/ci.yml/badge.svg)](https://github.com/optivisionlab/labs/actions/workflows/ci.yml)

Đây là kho lưu trữ mã nguồn cho trang web tĩnh của **OptiVisionLab**, được xây dựng bằng [MkDocs](https://www.mkdocs.org/) và theme [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

Trang web được triển khai tự động lên GitHub Pages tại: [https://optivisionlab.github.io/labs/](https://optivisionlab.github.io/labs/)

## Giới thiệu

Trang web này đóng vai trò là cổng thông tin chính thức của OptiVisionLab, giới thiệu về các hoạt động nghiên cứu, các ấn phẩm khoa học, thành viên, sản phẩm và bộ dữ liệu mà lab đã công bố.

## Phát triển cục bộ

Để chạy trang web trên máy tính của bạn, hãy làm theo các bước sau:

1.  **Clone kho lưu trữ:**
    ```bash
    git clone https://github.com/optivisionlab/labs.git
    cd labs
    ```

2.  **Cài đặt các gói cần thiết:**
    Đảm bảo bạn đã cài đặt Python và pip.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Chạy máy chủ phát triển:**
    ```bash
    mkdocs serve
    ```
    Trang web sẽ có sẵn tại `http://127.0.0.1:8000`. Máy chủ sẽ tự động tải lại mỗi khi có thay đổi trong mã nguồn.

## Triển khai

Quá trình triển khai được tự động hóa bằng GitHub Actions. Mỗi khi có một commit mới được đẩy lên nhánh `main`, workflow tại `.github/workflows/ci.yml` sẽ được kích hoạt. Workflow này sẽ:
1.  Cài đặt môi trường cần thiết.
2.  Xây dựng trang web tĩnh.
3.  Đẩy các tệp tĩnh đã xây dựng lên nhánh `gh-pages`.

GitHub Pages sau đó sẽ tự động phục vụ trang web từ nhánh `gh-pages`.
