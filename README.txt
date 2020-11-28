INT3401-8 - PROJECT 4: GHOSTBUSTERS

Question 1 (3 points): Exact Inference Observation
Bài toán yêu cầu mình phải cập nhật hàm sinh belief cho Pacman để dự đoán vị trí mà Ghost có thể đi tới dựa trên khoảng cách với chúng và vị trí của Pacman

Trong đó noisyDistance là khoảng cách Manhattan từ Pacman đến con ma đang truy đuổi, và nếu nó bằng 0 nghĩa là Pacman đã ăn được con ma, và đẩy con ma vào tù allPossible[jail] = 1.0
P(noisyDistance | TrueDistance)

Question 2 (4 points): Exact Inference with Time Elapse
Yêu cầu cập nhật belief dự đoán vị trí của Ghost từ thời gian t + 1 khi biết vị trí của nó ở thời gian t, dựa trên chướng ngại vật trên bản đồ (tường)

Sử dụng hàm self.getPositionDistribution(self.setGhostPosition(gameState, oldPos)) để xác định phân bố vị trí tiếp theo của Ghost khi biết vị trí hiện tại
Cập nhật dựa trên belief và phân bố vị trí mới Ghost có thể đi

Question 3 (3 points): Exact Inference Full Test
Yêu cầu tìm kiếm vị trí mà Ghost có thể ở đó, rồi lựa chọn hành động để Pacman có thể tiến gần đến Ghost gần nhất

Tạo PriorityQueue chứa Ghost gần nhất với Pacman
Tính khoảng cách giữa Pacman và Ghost gần nhất cho tất cả 4 hướng (NORTH, SOUTH, EAST & WEST)
So sánh 4 hướng đi xem hướng đi nào đưa Pacman đến gần với Ghost nhất và gần hơn vị trí hiện tại thì lựa chọn
Thuật toán dừng khi mà cả 4 hướng đi đều đưa Pacman đến xa với vị trí Ghost gần nhất

Question 4 (3 points): Approximate Inference Observation

Question 5 (4 points): Approximate Inference with Time Elapse

Question 6 (4 points): Joint Particle Filter Observation

Question 7 (4 points): Joint Particle Filter with Elapse Time

