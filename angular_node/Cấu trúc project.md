## Cấu trúc project 

Khi bạn sử dụng CLI command để tạo project bằng lệnh
```shell 
    ng new <ten project>

```

- Một dự án với thư mục gốc có tên là ```<ten project>``` mà bạn tạo
- Một test project end to end (e2e)
- Tập tin cấu hình liên quan 

## Những tập tin trong project

1. Tệp tin cấu hình cho các trình soạn thảo
```
    .editorconfig
```
2. Tệp chỉ định bỏ qua một số file khi upload mã nguồn của bạn nên github 

```
    .gitignore 
```
3. Tệp tin cấu hình CLI mặc định cho tất cả dự án trong working dir 

```
    angular.json 
```
4. cung cấp các npm package cho working dir 
```
    node_modeles 
```
5. Cấu hình npm package cho working space 
```
    package.json
```
6. Cung cấp thông tin version cho tất cả các package install trong node_modules 
```
    package-lock.json 
```
7. cấu hình typescript mặc định 
```
tsconfig.json 
```
8. Cấu hình TSLint mặc định
```
tslint.json
```
9. intro của document 
```
    README.md
```
