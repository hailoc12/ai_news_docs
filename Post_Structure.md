``` javascript
const post_structure = {
	id: 990,
	// Id của post, (Integer)
	authorId: '95d4e729-ff66-4428-b918-f01e8a49f1e8',
	// Id của tác giả (UUIDV4)
	title: 'Tui cũng vầy nè. Tui thích những bộ Tui cũng vầy nè',
	// Nếu là tin bài báo thì title là string
	// Nếu là tin mạng xã hội thì title null
	displayType: 0,
	// Kiểu hiển thị 0:Tin bài báo hoặc 1:Tin mạng xã hội
	featureImages: [
		'https://scontent.fhan3-1.fna.fbcdn.net/v/t1.0-0/p235x165/57104150_10214495057472161_7305707463183958016_n.jpg?_nc_cat=110&_nc_oc=AQniw6Gnl9MofZqtebVpfE30-NWT4As8Oq2_a17Vpup8muKL3FdC1Tt6DCyiUd_st0Q&_nc_ht=scontent.fhan3-1.fna&oh=b0a67b66f4a817f12d66a04f5e8262fb&oe=5D6EEA3B'
	],
	// Mảng các link ảnh [String]
	// Nếu là tin bài báo featureImages chỉ chứa 1 link ảnh
	// Nếu là tin mạng xã hội featureImages chỉ chứa 0,1 hoặc nhiều link ảnh
	createdAt: '2019-05-07T10:50:33.000Z',
	// Timestamp bài báo được viết lúc nào
	categories: [
		5,
		6,
		8,
	],
	// Mảng các Id của category [Integer]
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
			link: 'https://image.thanhnien.vn/660/uploaded/vubang/2019_04_24/tham-sat-binh-duong-3_lutz.jpg',
			// link image
		},
		{
			type: 'text',
			content: 'Thông tin ban đầu, vụ thảm sát được phát hiện trong sáng nay 24.4, lúc khoảng 7 giờ, tại khu phố Tân Ba, P.Thái Hòa, TX.Tân Uyên, Bình Dương.\n\nĐại tá Trịnh Ngọc Quyên, Giám đốc Công an Bình Dương, đã trực tiếp có mặt tại hiện trường, chỉ đạo điều tra phá án.',
		},
		{
			type: 'image',
			link: 'https://image.thanhnien.vn/660/uploaded/vubang/2019_04_24/tham-sat-binh-duong-1_bjhe.jpg',
		},
		{
			type: 'text',
			content: 'Cũng theo thông tin ban đầu, các nạn nhân được xác định là bà ngoại (tên Cúc) và hai cháu ngoại.\n\nVụ việc được phát hiện khi một người con gái của bà Cúc đi làm về thì điếng người phát hiện mẹ và hai cháu tử vong. Nhận định ban đầu từ cơ quan chức năng, đây là một vụ án giết người cướp tài sản.\n\nThông tin ban đầu từ cơ quan điều tra, các nạn nhân gồm: Đào Thị Thu Cúc (54 tuổi, bà ngoại); Trần Thị Quỳnh Nhi (17 tuổi), Nguyễn Thị Bảo Ngân (7 tuổi, cùng là cháu ngoại của bà Cúc).\n\nCũng theo thông tin ban đầu, cháu Bảo Ngân ở gần nhà ngoại, tối 23.4 có qua ngủ với bà ngoại thì gặp nạn.\n\nThanh Niên sẽ tiếp tục cập nhật',
		},
	],
	// Nếu là tin bài báo thì content là 1 mảng các object {type,content,link}
	// Nếu là tin mạng xã hội thì content là 1 string text.
};

// -------------------------------------------------------------

const example_news = {
	id: 988,
	authorId: 'f0bf4797-fa2d-4202-a741-681104439518',
	title: null,
	displayType: 1,
	featureImages: [
		'https://scontent.fhan3-1.fna.fbcdn.net/v/t1.0-0/p235x165/57104150_10214495057472161_7305707463183958016_n.jpg?_nc_cat=110&_nc_oc=AQniw6Gnl9MofZqtebVpfE30-NWT4As8Oq2_a17Vpup8muKL3FdC1Tt6DCyiUd_st0Q&_nc_ht=scontent.fhan3-1.fna&oh=b0a67b66f4a817f12d66a04f5e8262fb&oe=5D6EEA3B',
		'https://scontent.fhan3-2.fna.fbcdn.net/v/t1.0-0/p235x165/56209467_132725541134701_3838937495395893248_n.jpg?_nc_cat=103&_nc_oc=AQnzdV1ffgQwZsMv-l1FBep33vW86jrCSk3gwXw3wAEtszk1B35WM63l-1TRTRjt74g&_nc_ht=scontent.fhan3-2.fna&oh=0bba6694f453ad3fb024ca2f73a70f87&oe=5D2B9EE4',
		'https://scontent.fhan3-3.fna.fbcdn.net/v/t1.0-0/s526x296/55759798_132725507801371_3208767653069979648_n.jpg?_nc_cat=108&_nc_oc=AQm8GxUs3w6Y1pFgK7jXB49rcVTxR9tBykAWOA57ZWWgX9IILrOJRru2HhzD7OaysEc&_nc_ht=scontent.fhan3-3.fna&oh=2bc52bc54e8356e59891a9fc3023033d&oe=5D73CBB2',
		'https://scontent.fhan3-1.fna.fbcdn.net/v/t1.0-0/q92/p261x260/57379431_139876470419608_8129178291555794944_n.jpg?_nc_cat=111&_nc_oc=AQkhR1eE9Ny5cU1fMVlnkZ030uY8-220QAZmqWMei6jADhTt9Ba4rdamSQ8kzuQuKx0&_nc_ht=scontent.fhan3-1.fna&oh=f9e8a380a0f9c3479bbc7a775bd91141&oe=5D703380',
		'https://scontent.fhan4-1.fna.fbcdn.net/v/t1.0-0/p235x350/57094348_10214495055112102_907792259141861376_n.jpg?_nc_cat=104&_nc_oc=AQn4raWOkZ23zH6OMs5iAzr-zHNubyVtYFpynMLcJDGB3Wilbe1q0u1p7XHePO9PdbU&_nc_ht=scontent.fhan4-1.fna&oh=ec90a8cbd67156d4ea386ece0ccaf491&oe=5D745DDA',
	],
	createdAt: '2019-05-07T10:50:33.000Z',
	categories: [3, 5, 7],
	content: 'VIỆT NAM CÓ GÌ HAY\n\nTừ ngày dùng facebook thấy có khá nhiều bạn có cái nhìn thiếu tích cực về Việt Nam, nào là quốc gia nghèo khó, thu nhập đầu người thấp, kinh tế càng ngày càng tụt hậu, tham nhũng tràn lan, giáo dục lạc hậu, y tế quá tải, giao thông ùn tắc, không khí ô nhiễm, thực phẩm bẩn, độc hại..., từ đó một số bạn khái quát là “đến cái cột điện mà biết đi cũng bỏ nước mà ra đi”.\n\nThế nhưng thực tế là chúng ta và hơn 95 triệu người dân Việt Nam vẫn đang hàng ngày sinh sống, học tập và làm việc trên đất nước Việt Nam này.\n\nSống ở một quốc gia, sống ở một xã hội mà không yêu quí nó, không trân trọng nó, suốt ngày bới lông tìm vết, tìm điểm xấu, tìm cái dở để chỉ trích, chê bai, dè bỉu thì đúng là không thể hạnh phúc; sống như thế thì khổ lắm, không những khổ mình mà còn khổ gia đình, người thân, bạn bè, đồng nghiệp, khổ cả những người xung quanh nữa.\n\nChính vì vậy tôi đi tìm các điểm tích cực, các điểm tốt, xem Việt Nam liệu có gì hay, có gì tốt để cuộc sống thêm lạc quan, thêm hạnh phúc. Hay tốt ở đây là hay tốt theo chuẩn quốc tế, được các tổ chức quốc tế ghi nhận bằng những số liệu khách quan, chứ không phải hay theo kiểu tự sướng.\n\nSau đây là những điểm hay, điểm tốt của Việt Nam được các tổ chức quốc tế ghi nhận:\n1. Đất nước không có khủng bố: đứng số 1 thế giới\n2. Tác động kinh tế của bạo lực và xung đột: thấp thứ 21 thế giới\n3. Số người chết vì cháy nổ: thấp thứ 24 thế giới\n4. Tội phạm giết người: Trong nhóm 25% thấp nhất thế giới\n5. Chết vì tự tử: Trong nhóm 35% thấp nhất thế giới\n6. Tăng trưởng kinh tế: Thuộc top 5 quốc gia cao nhất thế giới\n7. Hạnh phúc và hài lòng với cuộc sống: Thứ 95 hay top 5 quốc gia hạnh phúc\n\nĐẤT NƯỚC KHÔNG CÓ KHỦNG BỐ\n\nTheo diễn đàn kinh tế thế giới WEF, Việt Nam là quốc gia không có tổ chức khủng bố, năm 2018 được 100 điểm tuyệt đối, cùng 21 quốc gia xếp số 1 thế giới về an ninh.\n\nTheo Viện kinh tế và hoà bình IEP (Úc), tính 20 năm (1998-2017), Việt Nam được xếp hạng 104 trên 138 quốc gia trong danh sách quốc gia về tội phạm khủng bố. Các bạn có biết trong khi đó Mỹ, Anh, Pháp, Đức, Canada, Úc, Nhật và một số nước châu Âu giàu có khác lại đứng thứ 20 đến 68 trong danh sách các quốc gia khủng bố, với điểm số cao gấp Việt Nam từ 5 đến 10 lần. Trong Asean Philippines, Thái Lan, Myanmar, Indonesia, Malaysia lần lượt xếp thứ 10, 17, 24, 42 và 70 thế giới, với điểm số cao gấp Việt Nam từ 4 đến 11 lần.\n\nBẠO LỰC VÀ XUNG ĐỘT\n\nTheo Viện kinh tế và Hoà bình IEP (Úc), Việt Nam được xếp thứ 21 trên 163 quốc gia về tiêu chí kinh tế ít chịu tác động của bạo lực và xung đột, trong khi đó Mỹ, Anh, Pháp, Úc, Ba Lan, Hungary, Hàn Quốc, Singapore... đều bị tác động lớn hơn Việt Nam rất nhiều.\n\nCHÁY NỔ VÀ GIẾT NGƯỜI\n\nTheo tổ chức Y tế thế giới WHO, Việt Nam được xếp thứ 24 trên 183 quốc gia có tỷ lệ chết người do cháy nổ thấp nhất thế giới.\n\nTheo diễn đàn kinh tế thế giới WEF, Việt Nam được xếp hạng 49 trên 140 quốc gia, tính theo số vụ giết người thấp nhất thế giới.\n\nTỰ TỬ\n\nTheo tổ chức Y tế thế giới WHO, Việt Nam thuộc top 35% quốc gia ít tự tử (đứng thứ 126 trên 183 quốc gia, tính theo số người chết do tự tử trong 100.000 dân).\n\nĐiểm rất lạ là các nước Âu, Mỹ, Hàn Quốc, Nhật Bản... lại có số người chết do tự tử cao hơn, thậm chí rất cao. Các nước giàu có có số người chết do tự tử cao có thể kể đến Hàn Quốc (cao thứ 10 thế giới), Bỉ (22), Nhật Bản (26), Phần Lan(36), Thuỵ Điển (42), Pháp (45), Mỹ (47), New Zealand (52), Áo (62), Thuỵ Sĩ (75), Úc (84), Hà Lan, Na Uy, Đan Mạch.... Bên cạnh chúng ta Thái Lan xếp thứ 44 và Singapore xếp thứ...\n\nHoá ra không phải cứ giàu có là hạnh phúc.\n\nTĂNG TRƯỞNG KINH TẾ CAO\n\nTheo con số thống kê của các tổ chức quốc tế (WB, IMF, UN...), Việt Nam thuộc top 5 quốc gia có tốc độ tăng trưởng kinh tế (GDP đầu người) cao nhất thế giới trong vòng 25 năm (1991-2016).\n\nTrong 25 năm (1991-2016), mức sống của người dân Việt Nam đã được nâng lên 3.87 lần, chỉ sau các nước Guinea xích đạo, Trung Quốc, Myanmar và Iraq. Cũng trong khoảng thời gian này Mỹ, Anh, Đức, Pháp, Nhật Bản, Canada, Úc, Italy và các nước Tây Âu chỉ nâng được có 1.15 đến 1.69 lần, còn các nước Asean như Philippines, Thái Lan, Indonesia, Malaysia, Singapore chỉ nâng lên được có 1.86, 2.20, 2.22, 2.28 và 2.32 lần.\n\nĐiểm này quan trọng lắm. Cuộc sống cứ năm nay tốt hơn năm trước, ngày hôm nay tốt hơn ngày hôm qua là vui, là hạnh phúc, còn cứ dậm chân tại chỗ, hoặc thụt lùi thì ai cũng không vui cả, kể cả người giàu.\n\n(tiếp: Việt Nam có là quốc gia Hạnh phúc)',
};

// --------------------------------------------------------------------------

const example_news_social = {
	id: 980,
	authorId: 'fdc82cb7-32c9-4d0f-a198-46b879de6ee1',
	title: 'Lượm được trên reddit. Thấy Google Assistant đang hot',
	featureImages: [
		'https://scontent.fhan3-1.fna.fbcdn.net/v/t1.0-0/s261x260/54434644_130300471377208_1019489974665347072_n.jpg?_nc_cat=111&_nc_oc=AQn0tpgC7PeNEbFYG-iSKngFyFrnSPxczPwVJU7mzUHVwwjnfpismdy5Xq67wdm5Vws&_nc_ht=scontent.fhan3-1.fna&oh=70c01c004771fc037a8dd4aacf955ef8&oe=5D63AE56'
	],
	displayType: 0,
	createdAt: '2019-05-07T10:50:33.000Z',
	content: [
		{
			type: 'text',
			content: 'Vụ thảm sát được phát hiện sáng 24.4 ở Bình Dương. 3 bà cháu tử vong trong nhà, trên người các nạn nhân có nhiều vết thương.',
		},
		{
			type: 'image',
			link: 'https://image.thanhnien.vn/660/uploaded/vubang/2019_04_24/tham-sat-binh-duong-3_lutz.jpg',
		},
		{
			type: 'text',
			content: 'Thông tin ban đầu, vụ thảm sát được phát hiện trong sáng nay 24.4, lúc khoảng 7 giờ, tại khu phố Tân Ba, P.Thái Hòa, TX.Tân Uyên, Bình Dương.\n\nĐại tá Trịnh Ngọc Quyên, Giám đốc Công an Bình Dương, đã trực tiếp có mặt tại hiện trường, chỉ đạo điều tra phá án.',
		},
		{
			type: 'image',
			link: 'https://image.thanhnien.vn/660/uploaded/vubang/2019_04_24/tham-sat-binh-duong-1_bjhe.jpg',
		},
		{
			type: 'text',
			content: 'Cũng theo thông tin ban đầu, các nạn nhân được xác định là bà ngoại (tên Cúc) và hai cháu ngoại.\n\nVụ việc được phát hiện khi một người con gái của bà Cúc đi làm về thì điếng người phát hiện mẹ và hai cháu tử vong. Nhận định ban đầu từ cơ quan chức năng, đây là một vụ án giết người cướp tài sản.\n\nThông tin ban đầu từ cơ quan điều tra, các nạn nhân gồm: Đào Thị Thu Cúc (54 tuổi, bà ngoại); Trần Thị Quỳnh Nhi (17 tuổi), Nguyễn Thị Bảo Ngân (7 tuổi, cùng là cháu ngoại của bà Cúc).\n\nCũng theo thông tin ban đầu, cháu Bảo Ngân ở gần nhà ngoại, tối 23.4 có qua ngủ với bà ngoại thì gặp nạn.\n\nThanh Niên sẽ tiếp tục cập nhật',
		},
	],
	categories: [3, 8, 10],
};
```
