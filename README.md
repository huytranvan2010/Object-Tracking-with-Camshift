Trong bài trước chúng ta đã tìm hiểu về object tracking với meanshift. Meanshift có vấn đề là kích thước của window không đổi trong suốt quá trình tracking dù vật ở xa hay gần camera. Một giải pháp ra đời có tên là CAMshift (continously Adaptive Meanshift).

CAMshift đầu tiên vẫn áp dụng Meanshift trước. Sau đó khi Meanshift hội tụ nó sẽ update kích thước của window, nó cũng tính tới hướng để khớp tốt nhất. Sau đó nó lại áp dụng meanshift cho window đã được scale với vị trí window trước. Quá trình cứ tiếp tục cho đến khi đạt được độ chính xác yêu cầu.

<img src="https://docs.opencv.org/master/camshift_face.gif" style="display:block margin-left:auto; margin-right:auto">