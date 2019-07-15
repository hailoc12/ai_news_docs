### Cấu trúc của post

``` javascript
const post_structure = {
	id: '997855787078548',
	// Id của post, (String), dài không quá 100 kí tự
	authorId: '270139599850174', dài không quá 100 ký tự
	// Id của tác giả (String), 
	title: 'Tui cũng vầy nè. Tui thích những bộ Tui cũng vầy nè',
	// Nếu là tin bài báo thì title là string
	// Nếu là tin mạng xã hội thì title null
	// title không được trống và chứa không quá 800 ký tự
	displayType: 0,
	// Kiểu hiển thị 0:Tin bài báo hoặc 1:Tin mạng xã hội
	tag: [
		{
			tag: 'Chiến thắng điện biên phủ chấn động địa cầu lừng lẫy năm châu 7/1954',
			// name của group (String), dài không quá 600 kí tự
			point: 10,
			// trọng số group (Number), số tự nhiên [1,1000]
		},
		{
			tag: 'Loạn 64 sứ quân',
			point: 9,
		},
	],
	// mảng các group của bài viết [{tag: String,point: Number}]
	featureImages: [
	    {
	      large:"https://i-vnexpress.vnecdn.net/2019/07/14/thu-ha-2647-1563099674.jpg",
	      small:"https://i-vnexpress.vnecdn.net/2019/07/14/bao1-8955-1563105780.jpg",
	    },
	],
	// Mảng các link ảnh [ { large , small } ]
	// Nếu là tin bài báo featureImages chỉ chứa 1 ảnh
	// Nếu là tin mạng xã hội featureImages chỉ chứa 0,1 hoặc nhiều ảnh
	createdAt: '2019-05-07T10:50:33.000Z',
	// Timestamp bài báo được viết lúc nào
	categories: [
		'amnhac',
		'amthuc',
		'bongda',
	],
	// Mảng các Id của category [String], mỗi id dài không quá 50 kí tự
	content: [
		{
			type: 'text',
			// kiểu data [text,image]
			content: 'Vụ thảm sát được phát hiện sáng 24.4 ở Bình Dương. 3 bà cháu tử vong trong nhà, trên người các nạn nhân có nhiều vết thương.',
			// content text
		},
		{
			type: 'image',
			// kiểu data [text,image]
			link: {
	      large:"https://i-vnexpress.vnecdn.net/2019/07/14/thu-ha-2647-1563099674.jpg",
	      small:"https://i-vnexpress.vnecdn.net/2019/07/14/bao1-8955-1563105780.jpg",
	    },
			// link image
		},
		{
			type: 'text',
			content: 'Thông tin ban đầu, vụ thảm sát được phát hiện trong sáng nay 24.4, lúc khoảng 7 giờ, tại khu phố Tân Ba, P.Thái Hòa, TX.Tân Uyên, Bình Dương.\n\nĐại tá Trịnh Ngọc Quyên, Giám đốc Công an Bình Dương, đã trực tiếp có mặt tại hiện trường, chỉ đạo điều tra phá án.',
		},
		{
			type: 'image',
			link: {
	      large:"https://i-vnexpress.vnecdn.net/2019/07/14/thu-ha-2647-1563099674.jpg",
	      small:"https://i-vnexpress.vnecdn.net/2019/07/14/bao1-8955-1563105780.jpg",
	    },
		},
		{
			type: 'text',
			content: 'Cũng theo thông tin ban đầu, các nạn nhân được xác định là bà ngoại (tên Cúc) và hai cháu ngoại.\n\nVụ việc được phát hiện khi một người con gái của bà Cúc đi làm về thì điếng người phát hiện mẹ và hai cháu tử vong. Nhận định ban đầu từ cơ quan chức năng, đây là một vụ án giết người cướp tài sản.\n\nThông tin ban đầu từ cơ quan điều tra, các nạn nhân gồm: Đào Thị Thu Cúc (54 tuổi, bà ngoại); Trần Thị Quỳnh Nhi (17 tuổi), Nguyễn Thị Bảo Ngân (7 tuổi, cùng là cháu ngoại của bà Cúc).\n\nCũng theo thông tin ban đầu, cháu Bảo Ngân ở gần nhà ngoại, tối 23.4 có qua ngủ với bà ngoại thì gặp nạn.\n\nThanh Niên sẽ tiếp tục cập nhật',
		},
	],
	// Nếu là tin bài báo thì content là 1 mảng các object {type,content,link}
	// Nếu là tin mạng xã hội thì content là 1 string text.
};
```

### Ví dụ tin bài báo

``` javascript
const example_news = {
	id: '270139599850174',
	authorId: '27112929982144',
	title: 'Lượm được trên reddit. Thấy Google Assistant đang hot',
	displayType: 0,
	tag: [
		{
			tag: 'Chiến thắng điện biên phủ chấn động địa cầu lừng lẫy năm châu 7/1954',
			point: 10,
		},
		{
			tag: 'Loạn 64 sứ quân',
			point: 9,
		},
	],
	featureImages: [
		{
	    large:"https://i-vnexpress.vnecdn.net/2019/07/14/thu-ha-2647-1563099674.jpg",
	    small:"https://i-vnexpress.vnecdn.net/2019/07/14/bao1-8955-1563105780.jpg",
	  },
	],
	createdAt: '2019-05-07T10:50:33.000Z',
	categories: ['amnhac', 'cntt', 'daotao'],
	content: [
		{
			type: 'text',
			content: 'Vụ thảm sát được phát hiện sáng 24.4 ở Bình Dương. 3 bà cháu tử vong trong nhà, trên người các nạn nhân có nhiều vết thương.',
		},
		{
			type: 'image',
			link: {
	      large:"https://i-vnexpress.vnecdn.net/2019/07/14/thu-ha-2647-1563099674.jpg",
	      small:"https://i-vnexpress.vnecdn.net/2019/07/14/bao1-8955-1563105780.jpg",
	    },
		},
		{
			type: 'text',
			content: 'Thông tin ban đầu, vụ thảm sát được phát hiện trong sáng nay 24.4, lúc khoảng 7 giờ, tại khu phố Tân Ba, P.Thái Hòa, TX.Tân Uyên, Bình Dương.\n\nĐại tá Trịnh Ngọc Quyên, Giám đốc Công an Bình Dương, đã trực tiếp có mặt tại hiện trường, chỉ đạo điều tra phá án.',
		},
		{
			type: 'image',
			link: {
	      large:"https://i-vnexpress.vnecdn.net/2019/07/14/thu-ha-2647-1563099674.jpg",
	      small:"https://i-vnexpress.vnecdn.net/2019/07/14/bao1-8955-1563105780.jpg",
	    },
		},
		{
			type: 'text',
			content: 'Cũng theo thông tin ban đầu, các nạn nhân được xác định là bà ngoại (tên Cúc) và hai cháu ngoại.\n\nVụ việc được phát hiện khi một người con gái của bà Cúc đi làm về thì điếng người phát hiện mẹ và hai cháu tử vong. Nhận định ban đầu từ cơ quan chức năng, đây là một vụ án giết người cướp tài sản.\n\nThông tin ban đầu từ cơ quan điều tra, các nạn nhân gồm: Đào Thị Thu Cúc (54 tuổi, bà ngoại); Trần Thị Quỳnh Nhi (17 tuổi), Nguyễn Thị Bảo Ngân (7 tuổi, cùng là cháu ngoại của bà Cúc).\n\nCũng theo thông tin ban đầu, cháu Bảo Ngân ở gần nhà ngoại, tối 23.4 có qua ngủ với bà ngoại thì gặp nạn.\n\nThanh Niên sẽ tiếp tục cập nhật',
		},
	],
};
```

### Ví dụ tin mạng xã hội

``` javascript
const example_news_social = {
	id: '270139599850174',
	authorId: '270139599850174',
	featureImages: [
    {
	    large:"https://i-vnexpress.vnecdn.net/2019/07/14/thu-ha-2647-1563099674.jpg",
	    small:"https://i-vnexpress.vnecdn.net/2019/07/14/bao1-8955-1563105780.jpg",
    },
    {
	    large:"https://i-vnexpress.vnecdn.net/2019/07/14/thu-ha-2647-1563099674.jpg",
	    small:"https://i-vnexpress.vnecdn.net/2019/07/14/bao1-8955-1563105780.jpg",
    },
    {
	    large:"https://i-vnexpress.vnecdn.net/2019/07/14/thu-ha-2647-1563099674.jpg",
	    small:"https://i-vnexpress.vnecdn.net/2019/07/14/bao1-8955-1563105780.jpg",
	  }
	],
	displayType: 1,
	tag: [
		{
			tag: 'Chiến thắng điện biên phủ chấn động địa cầu lừng lẫy năm châu 7/1954',
			point: 10,
		},
		{
			tag: 'Loạn 64 sứ quân',
			point: 9,
		},
	],
	createdAt: '2019-05-07T10:50:33.000Z',
	content: 'VIỆT NAM CÓ GÌ HAY\n\nTừ ngày dùng facebook thấy có khá nhiều bạn có cái nhìn thiếu tích cực về Việt Nam, nào là quốc gia nghèo khó, thu nhập đầu người thấp, kinh tế càng ngày càng tụt hậu, tham nhũng tràn lan, giáo dục lạc hậu, y tế quá tải, giao thông ùn tắc, không khí ô nhiễm, thực phẩm bẩn, độc hại..., từ đó một số bạn khái quát là “đến cái cột điện mà biết đi cũng bỏ nước mà ra đi”.\n\nThế nhưng thực tế là chúng ta và hơn 95 triệu người dân Việt Nam vẫn đang hàng ngày sinh sống, học tập và làm việc trên đất nước Việt Nam này.\n\nSống ở một quốc gia, sống ở một xã hội mà không yêu quí nó, không trân trọng nó, suốt ngày bới lông tìm vết, tìm điểm xấu, tìm cái dở để chỉ trích, chê bai, dè bỉu thì đúng là không thể hạnh phúc; sống như thế thì khổ lắm, không những khổ mình mà còn khổ gia đình, người thân, bạn bè, đồng nghiệp, khổ cả những người xung quanh nữa.\n\nChính vì vậy tôi đi tìm các điểm tích cực, các điểm tốt, xem Việt Nam liệu có gì hay, có gì tốt để cuộc sống thêm lạc quan, thêm hạnh phúc. Hay tốt ở đây là hay tốt theo chuẩn quốc tế, được các tổ chức quốc tế ghi nhận bằng những số liệu khách quan, chứ không phải hay theo kiểu tự sướng.\n\nSau đây là những điểm hay, điểm tốt của Việt Nam được các tổ chức quốc tế ghi nhận:\n1. Đất nước không có khủng bố: đứng số 1 thế giới\n2. Tác động kinh tế của bạo lực và xung đột: thấp thứ 21 thế giới\n3. Số người chết vì cháy nổ: thấp thứ 24 thế giới\n4. Tội phạm giết người: Trong nhóm 25% thấp nhất thế giới\n5. Chết vì tự tử: Trong nhóm 35% thấp nhất thế giới\n6. Tăng trưởng kinh tế: Thuộc top 5 quốc gia cao nhất thế giới\n7. Hạnh phúc và hài lòng với cuộc sống: Thứ 95 hay top 5 quốc gia hạnh phúc\n\nĐẤT NƯỚC KHÔNG CÓ KHỦNG BỐ\n\nTheo diễn đàn kinh tế thế giới WEF, Việt Nam là quốc gia không có tổ chức khủng bố, năm 2018 được 100 điểm tuyệt đối, cùng 21 quốc gia xếp số 1 thế giới về an ninh.\n\nTheo Viện kinh tế và hoà bình IEP (Úc), tính 20 năm (1998-2017), Việt Nam được xếp hạng 104 trên 138 quốc gia trong danh sách quốc gia về tội phạm khủng bố. Các bạn có biết trong khi đó Mỹ, Anh, Pháp, Đức, Canada, Úc, Nhật và một số nước châu Âu giàu có khác lại đứng thứ 20 đến 68 trong danh sách các quốc gia khủng bố, với điểm số cao gấp Việt Nam từ 5 đến 10 lần. Trong Asean Philippines, Thái Lan, Myanmar, Indonesia, Malaysia lần lượt xếp thứ 10, 17, 24, 42 và 70 thế giới, với điểm số cao gấp Việt Nam từ 4 đến 11 lần.\n\nBẠO LỰC VÀ XUNG ĐỘT\n\nTheo Viện kinh tế và Hoà bình IEP (Úc), Việt Nam được xếp thứ 21 trên 163 quốc gia về tiêu chí kinh tế ít chịu tác động của bạo lực và xung đột, trong khi đó Mỹ, Anh, Pháp, Úc, Ba Lan, Hungary, Hàn Quốc, Singapore... đều bị tác động lớn hơn Việt Nam rất nhiều.\n\nCHÁY NỔ VÀ GIẾT NGƯỜI\n\nTheo tổ chức Y tế thế giới WHO, Việt Nam được xếp thứ 24 trên 183 quốc gia có tỷ lệ chết người do cháy nổ thấp nhất thế giới.\n\nTheo diễn đàn kinh tế thế giới WEF, Việt Nam được xếp hạng 49 trên 140 quốc gia, tính theo số vụ giết người thấp nhất thế giới.\n\nTỰ TỬ\n\nTheo tổ chức Y tế thế giới WHO, Việt Nam thuộc top 35% quốc gia ít tự tử (đứng thứ 126 trên 183 quốc gia, tính theo số người chết do tự tử trong 100.000 dân).\n\nĐiểm rất lạ là các nước Âu, Mỹ, Hàn Quốc, Nhật Bản... lại có số người chết do tự tử cao hơn, thậm chí rất cao. Các nước giàu có có số người chết do tự tử cao có thể kể đến Hàn Quốc (cao thứ 10 thế giới), Bỉ (22), Nhật Bản (26), Phần Lan(36), Thuỵ Điển (42), Pháp (45), Mỹ (47), New Zealand (52), Áo (62), Thuỵ Sĩ (75), Úc (84), Hà Lan, Na Uy, Đan Mạch.... Bên cạnh chúng ta Thái Lan xếp thứ 44 và Singapore xếp thứ...\n\nHoá ra không phải cứ giàu có là hạnh phúc.\n\nTĂNG TRƯỞNG KINH TẾ CAO\n\nTheo con số thống kê của các tổ chức quốc tế (WB, IMF, UN...), Việt Nam thuộc top 5 quốc gia có tốc độ tăng trưởng kinh tế (GDP đầu người) cao nhất thế giới trong vòng 25 năm (1991-2016).\n\nTrong 25 năm (1991-2016), mức sống của người dân Việt Nam đã được nâng lên 3.87 lần, chỉ sau các nước Guinea xích đạo, Trung Quốc, Myanmar và Iraq. Cũng trong khoảng thời gian này Mỹ, Anh, Đức, Pháp, Nhật Bản, Canada, Úc, Italy và các nước Tây Âu chỉ nâng được có 1.15 đến 1.69 lần, còn các nước Asean như Philippines, Thái Lan, Indonesia, Malaysia, Singapore chỉ nâng lên được có 1.86, 2.20, 2.22, 2.28 và 2.32 lần.\n\nĐiểm này quan trọng lắm. Cuộc sống cứ năm nay tốt hơn năm trước, ngày hôm nay tốt hơn ngày hôm qua là vui, là hạnh phúc, còn cứ dậm chân tại chỗ, hoặc thụt lùi thì ai cũng không vui cả, kể cả người giàu.\n\n(tiếp: Việt Nam có là quốc gia Hạnh phúc)',
	categories: ['anninh', 'amthuc', 'amnhac'],
};
```
