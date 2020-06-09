# Android_Project
Apps Made by Cường241298
# Tải file apk về 
# Dùng Android Studio Import file -> tìm folder chứa hình ảnh các icon của ứng dụng.
# Phân tích apps 
- Chức năng nghe nhạc online, offline
- Chức năng tìm kiếm bài hát
- Fragment lời bài hát
- Tính năng tăng giảm âm lượng, tạm dừng, tiếp tục bài hát
- Tính năng đánh dấu bài hát yêu thích vào một danh mục yêu thích
- Tính năng tải nhạc online và nghe nhạc offline từ kho âm nhạc (API).
- Tính năng hẹn giờ phát (tắt) nhạc
- Tính năng nghe nhạc dưới nền thiết bị
- Tính năng đánh giá bài hát
- Tính năng phát bài nhạc ngẫu nhiên, lặp lại danh sách nhạc.
# Yêu cầu
- Mỗi người upload 10 bài hát dạng file mp3 nhạc vào folder data/music
- Thiết kế layout giao diện - theo như apps đã có - clone apps but shitier


# Phân tích thiết kế : Chỉ các lớp đối tượng
**** Model ****

- User : int id;
         String name;
         String username;
         String password;
- Music : int id_music_song;
          String title;
          String artist_name;
          String lyrics;
          TimeDate end;
- Comment : int id_comment;
            Time time;
            float star;
            String commt;
            int id_music;
            int id_user;
            
**** View ****

- Lấy nguyên si từ file apk, bên trong thư mục res/layout

**** Control ****

- int search_id_music(Music music) / Tìm kiếm bài hát
- Boolean check_login(User username, User password) / Kiểm tra đăng nhập
- Boolean check_alarm(Music music) / Kiểm tra hẹn giờ tắt bật nhạc
- Void choose_music(Music music) / Chọn bài hát
- Void add_music(Music music) / Thêm một bài hát
- Void random_list(ArrayList<Music> list) / Trộn ngẫu nhiên danh sách bài hát
- Void play_music(Music music) / Trình phát nhạc, kèm thêm chỉnh âm lượng bài hát
- Void rate_music(Music music) / Đánh giá bài hát
- ArrayList<Music> current_list() / Trả về danh sách bài hát hiện thời - chuẩn bị phát
- ArrayList<Music> download_music_list() / Trả về danh sách bài hát đã tải về
- ArrayList<Music> favorite_list() / Trả về danh sách bài hát yêu thích
- ArrayList<Comment> comment_list(Comment comment) / Trả về danh sách bình luận của bài hát
- Hàm gọi API đăng nhập của google và Facebook
  
