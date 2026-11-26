# Research Proposal

## 1. Project Title

Nghiên cứu và xây dựng ứng dụng mô phỏng các thuật toán tìm đường cho robot tự hành trong môi trường động có chướng ngại vật thay đổi.

**English:** Research and Development of a Pathfinding Simulation Application for Autonomous Robots in Dynamic Environments with Changing Obstacles.

## 2. Background and Motivation

Các thuật toán tìm đường như BFS, Dijkstra và A* được sử dụng phổ biến trong các bài toán tìm kiếm đường đi trên đồ thị.

Tuy nhiên, trong các ứng dụng thực tế như robot tự hành, môi trường di chuyển thường không cố định. Các chướng ngại vật có thể di chuyển, xuất hiện hoặc biến mất trong quá trình robot thực hiện hành trình.

Điều này đặt ra yêu cầu về khả năng cập nhật và lập kế hoạch lại đường đi một cách hiệu quả.

Dự án kế thừa ứng dụng tìm đường trên bản đồ Grid 2D của Project I và mở rộng sang môi trường động.

## 3. Research Objectives

- Xây dựng môi trường mô phỏng có chướng ngại vật động.
- Mô phỏng robot tự hành di chuyển trên bản đồ Grid 2D.
- Triển khai A*, Repeated A* và D* Lite.
- Xây dựng cơ chế phát hiện thay đổi và lập kế hoạch lại.
- So sánh hiệu năng các thuật toán.
- Phát triển giao diện trực quan bằng Python và Pygame.

## 4. Research Questions

RQ1: Làm thế nào để robot phát hiện và xử lý các thay đổi của môi trường?

RQ2: Repeated A* có những hạn chế gì khi phải thực hiện tìm kiếm lại nhiều lần?

RQ3: D* Lite có thể cải thiện hiệu năng lập kế hoạch lại so với Repeated A* không?

RQ4: Mức độ thay đổi của môi trường ảnh hưởng như thế nào đến hiệu năng các thuật toán?

## 5. Research Methodology

### Phase 1: Literature Review
Nghiên cứu các thuật toán tìm đường và lập kế hoạch lại.

### Phase 2: Environment Modeling
Xây dựng mô hình Grid và các loại chướng ngại vật.

### Phase 3: Algorithm Implementation
Triển khai A*, Repeated A* và D* Lite.

### Phase 4: Application Development
Xây dựng ứng dụng mô phỏng bằng Pygame.

### Phase 5: Experimental Evaluation
Thiết kế kịch bản và thu thập kết quả.

### Phase 6: Analysis and Conclusion
So sánh hiệu năng và đánh giá kết quả.

## 6. Evaluation Metrics

- Path Length.
- Planning Time.
- Replanning Time.
- Expanded Nodes.
- Number of Replanning Operations.
- Collision Count.
- Success Rate.

## 7. Expected Contributions

1. Mở rộng ứng dụng tìm đường từ môi trường tĩnh sang môi trường động.
2. Xây dựng cơ chế lập kế hoạch lại cho robot.
3. Triển khai và so sánh các phương pháp tìm đường.
4. Cung cấp công cụ mô phỏng trực quan phục vụ nghiên cứu thuật toán.

## 8. Technology Stack

- Programming Language: Python.
- Visualization: Pygame.
- Data Structures: Grid, Graph, Priority Queue, Heap.
- Testing: Python unittest hoặc pytest.
- Experimental Analysis: Pandas, Matplotlib.