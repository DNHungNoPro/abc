//---------------------------------------------- Bắt đầu xây dựng --------------------------------------------------
class _MyHomePageState extends State<MyHomePage>{

  //Khởi tạo lại hàm initState()
  @override
  void initState() {  //mục đích hàm này dùng để sự lý sự kiện trước khi hàm main được build ra
    // TODO: implement initState
    print('Đây là hàm initState');

    for(int i = 1; i <= 10; i++){
      total += i;      //gán total và tính tổng từ 1 đến 10
    }
    super.initState();  // gọi lại hàm initState() cha
  }

  // Xây dựng 1 đối tượng Widget tên là 'build' với giá trị kiểu 'BuildContext' là hàm chính
  @override
  Widget build(BuildContext context) {   
    print('Đây là hàm Main');
    return Scaffold(   //trả về 1 cái khung
        appBar: AppBar(
          title: Text(widget.title),
        ),
        body: Center(
          child: Text('Kết quả tổng từ 1 đến 10 = $total'),
        ),
    );
  }
  int total = 0;    
}
