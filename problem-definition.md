# Problem Definition – Dynamic Pathfinding

## 1. Problem Statement

Bài toán nghiên cứu việc tìm kiếm và cập nhật đường đi cho robot tự hành trong môi trường hai chiều dạng lưới (2D Grid), trong đó các chướng ngại vật có thể thay đổi vị trí, xuất hiện hoặc biến mất trong quá trình robot di chuyển.

Khác với bài toán tìm đường truyền thống trong môi trường tĩnh, robot không thể chỉ dựa vào một đường đi được tính toán từ ban đầu. Khi môi trường thay đổi và đường đi hiện tại không còn hợp lệ, hệ thống cần phát hiện sự thay đổi và thực hiện lập kế hoạch lại (Replanning).

Nghiên cứu tập trung vào việc xây dựng ứng dụng mô phỏng trực quan và so sánh hiệu quả của các phương pháp tìm đường, đặc biệt là A*, Repeated A* và D* Lite.

## 2. Input

- Bản đồ dạng lưới có kích thước M × N.
- Vị trí bắt đầu (Start).
- Vị trí đích (Goal).
- Danh sách chướng ngại vật tĩnh.
- Danh sách chướng ngại vật động.
- Quy tắc di chuyển của các chướng ngại vật.
- Thuật toán tìm đường được lựa chọn.

## 3. Output

- Đường đi từ Start đến Goal.
- Vị trí hiện tại của robot.
- Trạng thái các chướng ngại vật.
- Đường đi mới khi môi trường thay đổi.
- Trạng thái thành công hoặc thất bại của hành trình.
- Các thông số đánh giá hiệu năng thuật toán.

## 4. Environment Types

### 4.1. Static Environment
Các chướng ngại vật không thay đổi vị trí trong suốt quá trình mô phỏng.

### 4.2. Moving Obstacle Environment
Các chướng ngại vật di chuyển theo quỹ đạo xác định, chẳng hạn di chuyển ngang, dọc hoặc tuần hoàn.

### 4.3. Random Dynamic Environment
Các chướng ngại vật có thể xuất hiện hoặc biến mất tại những vị trí được lựa chọn ngẫu nhiên.

## 5. Main Challenges

1. Phát hiện sự thay đổi của môi trường.
2. Xác định đường đi hiện tại có còn hợp lệ hay không.
3. Tránh va chạm giữa robot và chướng ngại vật.
4. Tìm đường mới trong thời gian ngắn.
5. Giảm số lượng trạng thái phải xử lý lại.
6. Đảm bảo robot có thể tiếp tục hành trình nếu vẫn tồn tại đường đi hợp lệ.

## 6. Research Scope

Nghiên cứu tập trung vào ba thuật toán:

- A*: Baseline pathfinding algorithm.
- Repeated A*: Replanning by running A* again.
- D* Lite: Incremental heuristic search and replanning.

Ứng dụng được xây dựng bằng Python và Pygame, sử dụng môi trường Grid 2D để mô phỏng và đánh giá.

## 7. Assumptions and Constraints

- Robot di chuyển theo bốn hướng: lên, xuống, trái, phải.
- Mỗi bước di chuyển có chi phí bằng 1.
- Robot chỉ di chuyển vào các ô hợp lệ.
- Start và Goal không được trùng với chướng ngại vật.
- Robot cập nhật thông tin môi trường trước mỗi bước di chuyển.
- Mô phỏng sử dụng cơ chế cập nhật môi trường rời rạc theo từng bước thời gian.
- Phiên bản đầu tiên chưa mô phỏng động lực học hoặc cảm biến vật lý thực tế của robot.

## 8. Expected Results

Xây dựng được một ứng dụng có khả năng mô phỏng robot tìm đường trong môi trường động, phát hiện thay đổi của chướng ngại vật và cập nhật đường đi.

Đồng thời, đánh giá hiệu quả của A*, Repeated A* và D* Lite thông qua các kịch bản thực nghiệm khác nhau.