## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/sweetworm/graphal1062/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/sweetworm/graphal1062/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.





<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="description" content="">
    <meta name="author" content="">
    <link rel="icon"1032 href="./assets/ico/favicon.png">
	
    <title>1061 演算法教學網頁</title>

    <!-- Bootstrap core CSS -->
    <link href="./dist/css/bootstrap.min.css" rel="stylesheet">

    <!-- Custom styles for this template -->
    <link href="css/dashboard.css" rel="stylesheet">

    <!-- Just for debugging purposes. Don't actually copy these 2 lines! -->
    <!--[if lt IE 9]><script src="../../assets/js/ie8-responsive-file-warning.js"></script><![endif]-->

    <script src="./assets/js/ie-emulation-modes-warning.js"></script>
    <script type="text/javascript">

      var selectedSidebar = "#sidebar-li-01";
      var selectedTable = "#table-responsive-01";

      function initialize() {
        
        // 手動觸發popover第一次"click"事件
        $('#Contact').popover({trigger: 'click'});
        $('#HWFormat').popover({trigger: 'click'});
        $('#Others').popover({trigger: 'click'});

        // 處理左邊的sidebar被點擊時的反應
        $('ul.nav.nav-sidebar > li').on('click', function(){
          $(selectedTable).hide();
          $(selectedSidebar).removeAttr('class');
          $('.sub-header').empty();
          $('.sub-header').append($(this).text());
          var selectedLi = $(this).attr('id')[11]+$(this).attr('id')[12];
          selectedSidebar = "#sidebar-li-"+selectedLi;
          // console.log(selectedSidebar);

          // sidebar-li-01課程公告
          if (selectedSidebar != "#sidebar-li-01")
            $('.progress').hide();
          else
            $('.progress').show();

          if (selectedSidebar == "#sidebar-li-11")
            $('#table-responsive-08-2').show();
          else
            $('#table-responsive-08-2').hide();
            
          selectedTable = "#table-responsive-"+selectedLi;
          $(selectedSidebar).addClass('active');
          $(selectedTable).show();

        });

        // 處理右上角的navigational bar被點擊時的反應
        $('.nav.navbar-nav.navbar-right > li > a').on('click', function(){
          $(this).popover();
          // console.log($(this).parent().siblings().children().popover('hide'));
        });

        // 顯示課程講義PDF
        $('.pdf-title').on('click', function(){
          var pdfName = $(this).text()+".pdf";
          window.open("https://dl.dropboxusercontent.com/u/57606902/%E6%BC%94%E7%AE%97%E6%B3%95/"+pdfName, "_blank", 'width=850,height=750');
        });
        // 顯示作業PDF
       		$('.pdf-HW').on('click', function(){				  var pdfName = $(this).text();          window.open("https://dl.dropboxusercontent.com/u/57606902/%E6%BC%94%E7%AE%97%E6%B3%95/exercise/2012_algorithm_homework_"+pdfName.slice(8,10)+".pdf", "_blank", 'width=850,height=750');        });		$('.pdf-HW-sol').on('click', function(){				  var pdfName = $(this).text();          window.open("https://ba2c0e6c48b15d2c4a8b91bc72d796c454e7d356.googledrive.com/host/0B7tG2XFaB3uTcUwwWTlTYklkNlU/Homework%20"+pdfName.slice(3,6)+".pdf", "_blank", 'width=850,height=750');        });
		
		// 顯示考試解答
		$('.pdf-quiz_1').on('click', function(){
          window.open("https://drive.google.com/file/d/0B1WR0k8a4q5oX1BSaGtuU0szU2M/view?usp=sharing", "_blank", 'width=850,height=750');
        });
		$('.pdf-quiz_2').on('click', function(){
          window.open("https://drive.google.com/file/d/0B4EhR-vyuACTY0dEanF5dUZOUWM/view?usp=sharing", "_blank", 'width=850,height=750');
        });
		$('.pdf-quiz_3').on('click', function(){
          window.open("https://drive.google.com/file/d/0B1WR0k8a4q5oUmoyY0lFaXdtNlE/view?usp=sharing", "_blank", 'width=850,height=750');
        });
		$('.pdf-quiz_4').on('click', function(){
          window.open("https://drive.google.com/file/d/0B4EhR-vyuACTZ3lLSmJZb3ZzWVE/view?usp=sharing", "_blank", 'width=850,height=750');
        });
		$('.pdf-quiz_5').on('click', function(){
          window.open("https://drive.google.com/file/d/0B1WR0k8a4q5odHFxM1hxWmRqaVU/view?usp=sharing", "_blank", 'width=850,height=750');
        });
		$('.pdf-quiz_6').on('click', function(){
          window.open("https://drive.google.com/file/d/0B4EhR-vyuACTS1YzMjN4VGQ2YWs/view?usp=sharing", "_blank", 'width=850,height=750');
        });
		$('.pdf-quiz_7').on('click', function(){
          window.open("https://drive.google.com/file/d/0B1WR0k8a4q5oNEpOTHF5c2hDTHM/view?usp=sharing", "_blank", 'width=850,height=750');
        });
		$('.pdf-quiz_8').on('click', function(){
          window.open("https://drive.google.com/file/d/0B4EhR-vyuACTSGJKYUNBc3dzVDQ/view?usp=sharing", "_blank", 'width=850,height=750');
        });
		$('.pdf-quiz_9').on('click', function(){
          window.open("https://drive.google.com/file/d/0B1WR0k8a4q5odGFST3F6cDBPdE0/view?usp=sharing", "_blank", 'width=850,height=750');
        });
		$('.pdf-mid').on('click', function(){		  var pdfName = $(this).text();
          window.open("https://dl.dropboxusercontent.com/u/57606902/%E6%BC%94%E7%AE%97%E6%B3%95/AL-mid-"+pdfName.slice(2,4)+".pdf", "_blank", 'width=850,height=750');
        });				$('.pdf-final').on('click', function(){		  var pdfName = $(this).text();          window.open("https://dl.dropboxusercontent.com/u/57606902/%E6%BC%94%E7%AE%97%E6%B3%95/"+pdfName.slice(0,4)+"_NTOU_CSIE_algorithm_final.pdf", "_blank", 'width=850,height=750');        });		$('.pdf-exception').on('click', function(){		  var pdfName = $(this).text();          window.open("https://55244cb2399fc98701e30d1443f4e573489f446d.googledrive.com/host/0B7tG2XFaB3uTekpYTFRBd2pERVk/midterm_Q.pdf", "_blank", 'width=850,height=750');        });		
        // 設定 .table tbody tr & td 的style
        $('.nav.nav-sidebar').on('click', function(){
          $('.table tbody tr').css('height', '45px');
          $('.table tbody tr td').css('vertical-align', 'middle');
        });

        $('body').on('click', function (e) {
          $('[data-toggle="popover"]').each(function () {
          //the 'is' for buttons that trigger popups
          //the 'has' for icons within a button that triggers a popup
          if (!$(this).is(e.target) && $(this).has(e.target).length === 0 && $('.popover').has(e.target).length === 0) {
            $(this).popover('hide');
          }
        });

});

      };

    </script>
    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
  </head>

  <body onload="initialize()">

    <nav class="navbar navbar-inverse navbar-fixed-top">
      <div class="container-fluid">
        <div class="navbar-header">
          <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">
            <span class="sr-only">Toggle navigation</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <a class="navbar-brand" href="">1061 演算法教學網頁</a>
        </div>
        <div id="navbar" class="navbar-collapse collapse">
          <ul class="nav navbar-nav navbar-right">
            <!-- <li><button type="button" class="btn btn-lg btn-danger" data-toggle="popover" title="Popover title" data-content="And here's some amazing content. It's very engaging. Right?" data-placement="bottom">Click to toggle popover</button></li> -->
            <li><a href="#" id="Contact"  data-html="true" data-container="body" data-toggle="popover" data-placement="bottom" data-content="<font color='#E74425'>Teacher :</font><br>
                     林清池 INS509<br>
                     E-mail : lincc@mail.ntou.edu.tw<br><br>
                     <font color='#E74425'>TAs(資工) :</font><br>
                     劉閔正 INS601 6646<br>
                     任威竹 INS601 6646<br>
                     <font color='#E74425'>TA(電機) :</font><br>
                     吳志軒 INS603 6609<br>
                     ">聯絡資訊</a></li>
            <!--<li><a href="#" id="HWFormat" data-html="true" data-container="body" data-toggle="popover" data-placement="bottom" data-content="請用<font color='red'> 雙面空白A4紙書寫</font><br>
                     標明<font color='red'> HW# 姓名 學號</font><br>
                     未依格式者，不予計分">作業格式</a></li>-->
            <li><a href="#" id="Others" style="margin-right:100px" data-html="true" data-container="body" data-toggle="popover" data-placement="bottom" data-content="FB社團：<br><a href='https://www.facebook.com/groups/268978283595171/?fref=ts'>106海大演算法討論區</a><br><br>"
              >其他資訊</a></li>
          </ul>
          <!-- <form class="navbar-form navbar-right">
            <input type="text" class="form-control" placeholder="Search...">
          </form> -->
        </div>
      </div>
    </nav>

    <div class="container-fluid">
      <div class="row">
        <div class="col-sm-3 col-md-2 sidebar">
          <ul class="nav nav-sidebar">
            <!-- <li class="active" id="sidebar-li-1"><a href="#">課程公告<span class="sr-only">(current)</span></a></li> -->
            <li style="text-align:center; "; class="active" id="sidebar-li-01"><a href="#">課程公告</a></li>
            <li style="text-align:center;"; id="sidebar-li-02"><a href="#">上課講義</a></li>
            <li style="text-align:center;"; id="sidebar-li-03"><a href="#">作業下載</a></li>
            <li style="text-align:center;"; id="sidebar-li-04"><a href="#">考試題目</a></li>
			<li style="text-align:center;"; id="sidebar-li-05"><a href="#">發問紀錄(電機系)</a></li>
			<li style="text-align:center;"; id="sidebar-li-06"><a href="#">發問紀錄(資工系)</a></li>
			<li style="text-align:center;"; id="sidebar-li-07"><a href="#">補強紀錄(電機系)</a></li>
			<li style="text-align:center;"; id="sidebar-li-08"><a href="#">補強紀錄(資工系)</a></li>
      <li style="text-align:center;"; id="sidebar-li-09"><a href="#">成績查詢(電機系)</a></li>
      <li style="text-align:center;"; id="sidebar-li-10"><a href="#">成績查詢(資工系)</a></li>
            <li style="text-align:center;"; id="sidebar-li-12"><a href="#">程式練習</a></li>
            <!--<li style="text-align:center;"; id="sidebar-li-13"><a href="#">程式練習B</a></li>-->
			<li style="text-align:center;"; id="sidebar-li-14"><a href="#">期末總成績(電機系)</a></li>
			<li style="text-align:center;"; id="sidebar-li-15"><a href="#">期末總成績(資工系)</a></li>
 
            <li style="text-align:center;" id="sidebar-li-11"><a href="#">歷屆考題</a></li>
          </ul>
        </div>
        <div class="col-sm-9 col-sm-offset-3 col-md-10 col-md-offset-2 main">
          <h2 class="sub-header">課程公告</h2>
          <!-- <div class="progress">
            <div class="progress-bar progress-bar-striped active" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 60%;">
            60%
            </div>
            距離期中考還有...30天
          </div>
          <div class="table-responsive"> -->
          
          <!--..課程公告的顯示Table..-->
            <table class="table table-striped" id="table-responsive-01">
              <thead>
                <tr>
                  <th colspan="2" style="text-align:center;font-size:20px;width:25%">時間</th>
                  <th style="text-align:center;font-size:20px;width:70%">事由</th>
                </tr>
              </thead>
              <tbody>
                  <tr>    
                      <td style="text-align:left;vertical-align:middle"><span class="label label-danger">Important</span></td>
                      <td class="bulletin-date">2018/1/11</td>
                      <td style="text-align:center;vertical-align:middle;"><a href="https://goo.gl/CWc32e" target="_blank">電機系期末總成績表(更新)</a></td>
                  <tr>  
                  <tr>    
                    <td style="text-align:left;vertical-align:middle"><span class="label label-danger">new</span></td>
                      <td class="bulletin-date">2018/1/8</td>
                      <td style="text-align:center;vertical-align:middle;">期末考資訊:時間：1/9 (二) 晚上 6:00~9:00 地點：電機 B01 資工 B10 B12 範圍：第 8 章 ~ 第 16 章 可攜帶一張「手寫」 A4 紙張</td>
                </tr>
                   
                      <td style="text-align:left;vertical-align:middle"><span class="label label-danger">new</span></td>
                      <td class="bulletin-date">2017/11/24</td>
                      <td style="text-align:center;vertical-align:middle;"><a href="https://drive.google.com/file/d/1ygvtSfugPurgkl0TT_PNkAen-MlbiNnD/view?usp=sharing" target="_blank">12/07 跟 11/30的上課發問 11/07 小考成績(資工) </a></td>
                </tr>
                  <tr>    
                      <td style="text-align:left;vertical-align:middle"><span class="label label-danger"></span></td>
                      <td class="bulletin-date">2017/11/1</td>
                      <td style="text-align:center;vertical-align:middle;">期中考公告 時間:11/7(二)晚上 6:00~9:00 地點:B03、B10、B12 期中考範圍:第 0 章 ~ 第 8 章 counting sort</td>
                </tr>
                  <tr>    
                      <td style="text-align:left;vertical-align:middle"><span class="label label-danger"></span></td>
                      <td class="bulletin-date">2017/9/23</td>
                      <td style="text-align:center;vertical-align:middle;">助教地點:INS205 </td>
                </tr>
                <tr>    
                      <td style="text-align:left;vertical-align:middle"><span class="label label-danger"></span></td>
                      <td class="bulletin-date">2017/9/23</td>
                      <td style="text-align:center;vertical-align:middle;">助教時間: 每個禮拜二 下午5~6(9/26 助教時間為4~5點) 地點:在lab601 </td>
                </tr>

                <tr>    
                  <td style="text-align:left;vertical-align:middle"><span class="label label-danger"></span></td>
                  <td class="bulletin-date">2017/9/21</td>
                  <td style="text-align:center;vertical-align:middle;">請有修演算法週三早上的同學(有訂講義者)於下週9/27周三上課時帶110元向助教領取講義</td>
                </tr>

			          <tr>    
				          <td style="text-align:left;vertical-align:middle"><span class="label label-danger"></span></td>
				          <td class="bulletin-date">2017/9/15</td>
				          <td style="text-align:center;vertical-align:middle;">WEB TEST</td>
                </tr>

              </tbody>
            </table>
           
           <!--上課講義頁面-->
            <table class="table table-striped" id="table-responsive-02" style="display:none;">
              <thead>
                <tr>
                  <th class="title-font">章節名稱</th>
                  <th class="title-font">檔案下載</th>
                  <th class="title-font">列印格式</th>
                  <th class="title-font">筆記版本</th>
                  <th class="title-font">上傳日期</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td style="vertical-align:middle;">Syllabus</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/2QyrtH" target="_blank">Syllabus</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/LxuRD2" target="_blank">Syllabus-4</a></td>
                  <td style="vertical-align:middle;"></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
                <tr>
                  <td style="vertical-align:middle;">Ch0  Stable Matching</td>
                  <td style="vertical-align:middle;"><a href="http://goo.gl/PBSpqU" target="_blank">Algorithm-Ch0</a></td>
                 <td style="vertical-align:middle;"><a href="https://goo.gl/pTLAf5" target="_blank">Algorithm-Ch0-4</a></td>
                  <td style="vertical-align:middle;"></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
                <tr>
                  <td style="vertical-align:middle;">Ch1  Preliminaries</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/RTCHQk" target="_blank">Algorithm-Ch1</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/UrXtHs" target="_blank">Algorithm-Ch1-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/MA6fyU" target="_blank">Algorithm-Ch1-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
                <tr>
                  <td style="vertical-align:middle;">Ch2  Getting Started</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/LbkUGH" target="_blank">Algorithm-Ch2</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/uQXKG6" target="_blank">Algorithm-Ch2-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/wsXLsA" target="_blank">Algorithm-Ch2-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
                <tr>
                  <td style="vertical-align:middle;">Ch3  Growth of Functions</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/fmpD9p" target="_blank">Algorithm-Ch3</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/38qamw" target="_blank">Algorithm-Ch3-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/SqQ7Yv" target="_blank">Algorithm-Ch3-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
                <tr>
                  <td style="vertical-align:middle;">Ch4  Recurrences</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/bzZPhN" target="_blank">Algorithm-Ch4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/AUHiLX" target="_blank">Algorithm-Ch4-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/NKuosb" target="_blank">Algorithm-Ch4-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
                <tr>
                  <td style="vertical-align:middle;">Ch6 Heapsort</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/rQPQJL" target="_blank">Algorithm-Ch6</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/2gBAQx" target="_blank">Algorithm-Ch6-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/r9Mzv9" target="_blank">Algorithm-Ch6-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
                <tr>
                  <td style="vertical-align:middle;">Ch7 Quicksort</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/kLFCdD" target="_blank">Algorithm-Ch7</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/gpEkb6" target="_blank">Algorithm-Ch7-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/56d1a8" target="_blank">Algorithm-Ch7-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
                <tr>
                  <td style="vertical-align:middle;">Ch8 Sorting in Linear Time</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/dsTsnS" target="_blank">Algorithm-Ch8</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/X2qvQJ" target="_blank">Algorithm-Ch8-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/R1anVm" target="_blank">Algorithm-Ch8-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
				<tr>
                  <td style="vertical-align:middle;">Ch9 Medians and Order Statistics</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/Dfbrqh" target="_blank">Algorithm-Ch9</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/eK2FwG" target="_blank">Algorithm-Ch9-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/PEf8Ei" target="_blank">Algorithm-Ch9-annotated</a></td>
                 <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
				<tr>
                  <td style="vertical-align:middle;">Ch11 Hash Tables</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/awdhAJ" target="_blank">Algorithm-Ch11</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/jPv7gK" target="_blank">Algorithm-Ch11-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/cFzzxw" target="_blank">Algorithm-Ch11-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
				<tr>
                  <td style="vertical-align:middle;">Ch12 Binary Search Trees</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/CkL4zR" target="_blank">Algorithm-Ch12</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/ddxghA" target="_blank">Algorithm-Ch12-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/LXT7bv" target="_blank">Algorithm-Ch12-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
				<tr>
                  <td style="vertical-align:middle;">Ch13 Red Black Trees</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/AS6hsq" target="_blank">Algorithm-Ch13</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/idbP9P" target="_blank">Algorithm-Ch13-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/cKto4U" target="_blank">Algorithm-Ch13-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>
				<tr>
                  <td style="vertical-align:middle;">Ch15 Dynamic Programming</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/mTJjQe" target="_blank">Algorithm-Ch15</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/uKhPAq" target="_blank">Algorithm-Ch15-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/hShGTq" target="_blank">Algorithm-Ch15-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/15</td>
                </tr>								
				<tr>                  
				  <td style="vertical-align:middle;">Ch16 Greedy Algorithms</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/8FJHw7" target="_blank">Algorithm-Ch16</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/7Hbaic" target="_blank">Algorithm-Ch16-4</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/u4cguu" target="_blank">Algorithm-Ch16-annotated</a></td>
                  <td style="vertical-align:middle;">2017/09/08</td>                
				</tr>

				<!------動畫------>
				<tr>
                  <th class="title-font">動畫</th>
                </tr>
				
				<tr>
				  <td style="vertical-align:middle;"><a href="https://goo.gl/HOaEZa">QuickSort動畫</a></td>
                  <td style="vertical-align:middle;"><a href="#" class="pdf-title"></a></td>
                  <td style="vertical-align:middle;"><a href="#" class="pdf-title"></a></td>
                  <td style="vertical-align:middle;"><a href="#" class="pdf-title"></a></td>
                  <td style="vertical-align:middle;">2016/11/08</td> 
				</tr>
				
				
				
              </tbody>
            </table>
            

            <!--作業下載頁面開始-->
            <table class="table table-striped" id="table-responsive-03" style="display:none;">
              <thead>
                <tr>
                  <th class="title-font">週次</th>
                  <th class="title-font">作業</th>
                  <th class="title-font">解答</th>
                  <th class="title-font">上傳日期</th>
                </tr>
              </thead>
              
              <!--作業下載Table Tbody編輯部份-->
              <tbody>				
                <!--作業下載單一項目範例-->
                <tr>
                  <td style="vertical-align:middle;">3</td>
                  <td style="vertical-align:middle;"><a href="#" class="pdf-HW">Homework2</a></td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/XXV3aZ">Ans2</a></td>
                  <td style="vertical-align:middle;">2015/09/10</td>
                </tr>
                               

                
               			<tr>
					<td style="vertical-align:middle;">5</td>
					<td style="vertical-align:middle;"><a href="#" class="pdf-HW">Homework3</a></td>
					<td style="vertical-align:middle;"><a href="https://goo.gl/vwNOmW">Ans3</a></td>
					<td style="vertical-align:middle;">2015/09/10</td>
				</tr>
				<tr>
					<td style="vertical-align:middle;">5</td>
					<td style="vertical-align:middle;"><a href="#" class="pdf-HW">Homework4</a></td>
					<td style="vertical-align:middle;"><a href="https://goo.gl/tO1Y5x">Ans4</a></td>
					<td style="vertical-align:middle;">2015/09/10</td>
				</tr>
				<tr>
					<td style="vertical-align:middle;">8</td> 
					<td style="vertical-align:middle;"><a href="#" class="pdf-HW">Homework6</a></td>
					<td style="vertical-align:middle;"><a href="https://goo.gl/zK05Y1">Ans6</a></td>
					<td style="vertical-align:middle;">2015/09/10</td>
				</tr>
				<tr>
					<td style="vertical-align:middle;">8</td>
					<td style="vertical-align:middle;"><a href="#" class="pdf-HW">Homework7</a></td>
					<td style="vertical-align:middle;"><a href="https://goo.gl/kxLdRC">Ans7</a></td>
					<td style="vertical-align:middle;">2015/09/10</td>
				</tr>
                		<tr>
					<td style="vertical-align:middle;">12</td>
					<td style="vertical-align:middle;"><a href="#" class="pdf-HW">Homework8</a></td>
					<td style="vertical-align:middle;"><a href="https://goo.gl/1Ipkp7">Ans8</a></td>
					<td style="vertical-align:middle;">2015/09/10</td>
				</tr>
				<tr>
					<td style="vertical-align:middle;">12</td>
					<td style="vertical-align:middle;"><a href="#" class="pdf-HW">Homework9</a></td>
					<td style="vertical-align:middle;"><a href="https://goo.gl/bTwUcZ">Ans9</a><a href="https://goo.gl/kj4ymT">Ans9-5</a></td>
					<td style="vertical-align:middle;">2015/09/10</td>
				</tr>
				<tr>
					<td style="vertical-align:middle;">15</td>
					<td style="vertical-align:middle;"><a href="#" class="pdf-HW">Homework11</a></td>
					<td style="vertical-align:middle;"><a href="https://goo.gl/WfAinL">Ans11</a></td>
					<td style="vertical-align:middle;">2015/09/10</td>
				</tr>
				<tr>
					<td style="vertical-align:middle;">15</td>
					<td style="vertical-align:middle;"><a href="#" class="pdf-HW">Homework12</a></td>
					<td style="vertical-align:middle;"><a href="https://goo.gl/0kfXu3">Ans12</a></td>
					<td style="vertical-align:middle;">2015/09/10</td>
				</tr>
				<tr>
					<td style="vertical-align:middle;">16</td>
					<td style="vertical-align:middle;"><a href="#" class="pdf-HW">Homework13</a></td>
					<td style="vertical-align:middle;"><a href="https://goo.gl/gU7GkL" >Ans13</a></td>
					<td style="vertical-align:middle;">2015/09/10</td>
				</tr>
				<tr>
					<td style="vertical-align:middle;">17</td>
					<td style="vertical-align:middle;"><a href="#" class="pdf-HW">Homework15</a></td>
					<td style="vertical-align:middle;"><a href="https://goo.gl/sJwSAJ" >Ans15</a></td>
					<td style="vertical-align:middle;">2015/09/10</td>
				</tr>
                

              </tbody>
            </table>
            
            <!--考試題目頁面開始-->
			<table class="table table-striped" id="table-responsive-04" style="display:none;">
			<thead>                <tr>                  <!-- <th class="title-font">週次</th> -->                  <th class="title-font">名稱</th>                  <th class="title-font">解答</th>                  <th class="title-font">上傳日期</th>                </tr>              </thead>              
			
			<tbody>
          <tr>
              <td style="vertical-align:middle;">Quiz_1(電機)</td>
              <td style="vertical-align:middle;"><a href="https://drive.google.com/open?id=0BxJp5QcLMI49OXBlM0p3YUNTUnM">Quiz1_solution</a></td>
              <td style="vertical-align:middle;">2017/09/25</td>			
          </tr>
				<tr>
						<td style="vertical-align:middle;">Quiz_2(資工)</td>
						<td style="vertical-align:middle;"><a href="https://drive.google.com/open?id=0BxJp5QcLMI49dFJZSnNtc1RGTVk">Quiz2_solution</a></td>
						<td style="vertical-align:middle;">2017/10/02</td>			
				</tr>
		
				<tr>
						<td style="vertical-align:middle;">Quiz_3(資工)</td>
						<td style="vertical-align:middle;"><a href="https://drive.google.com/open?id=0BxJp5QcLMI49MkVETng2eWZBWGc">Quiz3_solution</a></td>
						<td style="vertical-align:middle;">2017/10/09</td>			
				</tr>
				<tr>
          <td style="vertical-align:middle;">Quiz_4(電機)</td>
          <td style="vertical-align:middle;"><a href="https://drive.google.com/open?id=0BxJp5QcLMI49MkVETng2eWZBWGc">Quiz3_solution</a></td>
          <td style="vertical-align:middle;">2017/10/23</td>			
      </tr>
				<tr>
						<td style="vertical-align:middle;">Quiz_5(資工)</td>
						<td style="vertical-align:middle;"><a href="https://drive.google.com/open?id=0BxJp5QcLMI49TGdVQlNjVFRsT00">Quiz5_solution</a></td>
						<td style="vertical-align:middle;">2017/10/21</td>			
				</tr>
        <tr>
          <td style="vertical-align:middle;">Quiz_5(電機)</td>
          <td style="vertical-align:middle;"><a href=" https://drive.google.com/open?id=0BxJp5QcLMI49YTA3RkJLRTRPSFE">Quiz5_solution</a></td>
          <td style="vertical-align:middle;">2017/10/26</td>			
      </tr>
      <tr>
        <td style="vertical-align:middle;">Quiz_7(資工)</td>
        <td style="vertical-align:middle;"><a href="https://drive.google.com/open?id=0BxJp5QcLMI49VEJaVTdDcVRXazA">Quiz7_solution</a></td>
        <td style="vertical-align:middle;">2017/11/06</td>			
    </tr>
    <tr>
      <td style="vertical-align:middle;">Quiz_7(電機)</td>
      <td style="vertical-align:middle;"><a href="https://goo.gl/Kf2Seb">Quiz7_solution</a></td>
      <td style="vertical-align:middle;">2017/11/30</td>			
  </tr>
  <tr>
    <td style="vertical-align:middle;">Quiz_8(電機)</td>
    <td style="vertical-align:middle;"><a href="https://drive.google.com/file/d/1Zkl4JBpeeVwWEM-386CnrhCBBtyBJkNS/view?usp=sharing">Quiz8_solution</a></td>
    <td style="vertical-align:middle;">2018/1/5</td>			
</tr>
<tr>
  <td style="vertical-align:middle;">Quiz_9(電機)</td>
  <td style="vertical-align:middle;"><a href="https://drive.google.com/file/d/1HwldLzY5jonC8_RAd_Veb8DrqCGleBn-/view?usp=sharing">Quiz9_solution</a></td>
  <td style="vertical-align:middle;">2018/1/5</td>			
</tr>
<tr>
  <td style="vertical-align:middle;">Quiz_9-1(電機)</td>
  <td style="vertical-align:middle;"><a href="https://drive.google.com/file/d/1kAchQazJmpTmvTVZ85gWiAQq90ePYF_b/view?usp=sharing">Quiz9-1_solution</a></td>
  <td style="vertical-align:middle;">2018/1/5</td>			
</tr>
<tr>
  <td style="vertical-align:middle;">Quiz_10(電機)</td>
  <td style="vertical-align:middle;"><a href="https://drive.google.com/file/d/1Esm_GH2fsz6KQzqm0eBIyPPOa3FHTFQc/view?usp=sharing">Quiz10_solution</a></td>
  <td style="vertical-align:middle;">2018/1/5</td>			
</tr>
<tr>
  <td style="vertical-align:middle;">Quiz_11(電機)</td>
  <td style="vertical-align:middle;"><a href="https://drive.google.com/open?id=1BhjBXXwqR4GTUoJFeF-wIR_AjbfTZWoa">Quiz11_solution</a></td>
  <td style="vertical-align:middle;">2018/1/5</td>			
</tr>
			<!--	<tr>
						<td style="vertical-align:middle;">Quiz5_FindMaxSubarray_MasterMethod</td>
						<td style="vertical-align:middle;"><a href="https://goo.gl/7p0sMK">Quiz5_solution</a></td>
						<td style="vertical-align:middle;">2016/10/27</td>			
				</tr>
				
				<tr>
						<td style="vertical-align:middle;">Quiz6-MaxHeap_ProveHeapHeight</td>
						<td style="vertical-align:middle;"><a href="https://goo.gl/vUfKKd">Quiz6_solution</a></td>
						<td style="vertical-align:middle;">2016/11/3</td>			
				</tr>
				
				<tr>
						<td style="vertical-align:middle;">Quiz7-Rods Cutting</td>
						<td style="vertical-align:middle;"><a href="https://goo.gl/o9Vmml">Quiz7_solution</a></td>
						<td style="vertical-align:middle;">2016/12/1</td>			
				</tr>

				<tr>
						<td style="vertical-align:middle;">Quiz8-Matrix Chain</td>
						<td style="vertical-align:middle;"><a href="https://goo.gl/pPwh5a">Quiz8_solution</a></td>
						<td style="vertical-align:middle;">2016/12/6</td>			
				</tr>

				<tr>
						<td style="vertical-align:middle;">Quiz9-Longest increasing subsequence</td>
						<td style="vertical-align:middle;"><a href="https://goo.gl/GB6gvP">Quiz9_solution</a></td>
						<td style="vertical-align:middle;">2016/12/13</td>			
				</tr>

				<tr>
						<td style="vertical-align:middle;">Quiz10-Minimizing lateness problem</td>
						<td style="vertical-align:middle;"><a href="https://goo.gl/btRJ3F">Quiz10_solution</a></td>
						<td style="vertical-align:middle;">2016/12/20</td>			
				</tr>

				<tr>
						<td style="vertical-align:middle;">Quiz11-RedBlack Tree</td>
						<td style="vertical-align:middle;"><a href="https://goo.gl/AqXc26">Quiz11_solution</a></td>
						<td style="vertical-align:middle;">2016/12/27</td>			
				</tr>

				<tr>
						<td style="vertical-align:middle;">Quiz12-RedBlack Tree Del</td>
						<td style="vertical-align:middle;"><a href="https://goo.gl/UIiKf8">Quiz12_solution</a></td>
						<td style="vertical-align:middle;">2017/01/03</td>			
				</tr>


				<tr>
						<td style="vertical-align:middle;">------</td>
						<td style="vertical-align:middle;"><a href="">分隔線</a></td>
						<td style="vertical-align:middle;">------</td>
				</tr>

				<tr>
						<td style="vertical-align:middle;">Ch4-Divide and Conquer</td>
						<td style="vertical-align:middle;"><a href="https://goo.gl/Zfl6KW">Problem_MaximumSubArray</a></td>
						<td style="vertical-align:middle;">2016/10/31</td>			
				</tr>

				<tr>
						<td style="vertical-align:middle;">Ch6-HeapSort</td>
						<td style="vertical-align:middle;"><a href="https://goo.gl/bq2E4N">Problem_Prove_MaxHeap_height_and_lastParent</a></td>
						<td style="vertical-align:middle;">2016/10/31</td>			
				</tr>
      -->
      


				
			</tbody>
			<!--註解開始，Table橫條內容
			<tbody>			  			                    
				<td style="vertical-align:middle;">第一次小考</td>				                    <td style="vertical-align:middle;"><a href="#" class="pdf-quiz_1">Quiz_1</a></td>                  <td style="vertical-align:middle;">2015/09/22</td>				              
			</tbody>
			<tbody>			  			                    
				<td style="vertical-align:middle;">第二次小考</td>				                    <td style="vertical-align:middle;"><a href="#" class="pdf-quiz_2">Quiz_2</a></td>                  <td style="vertical-align:middle;">2015/09/29</td>				              
			</tbody>
			<tbody>			  			                    
				<td style="vertical-align:middle;">第三次小考</td>				                    <td style="vertical-align:middle;"><a href="#" class="pdf-quiz_3">Quiz_3</a></td>                  <td style="vertical-align:middle;">2015/10/16</td>				              
			</tbody>
			<tbody>			  			                    
				<td style="vertical-align:middle;">第四次小考</td>				                    <td style="vertical-align:middle;"><a href="#" class="pdf-quiz_4">Quiz_4</a></td>                  <td style="vertical-align:middle;">2015/10/23</td>				              
			</tbody>
			<tbody>			  			                    
				<td style="vertical-align:middle;">第五次小考</td>				                    <td style="vertical-align:middle;"><a href="#" class="pdf-quiz_5">Quiz_5</a></td>                  <td style="vertical-align:middle;">2015/11/10</td>				              
			</tbody>
			<tbody>			  			                    
				<td style="vertical-align:middle;">第六次小考</td>				                    <td style="vertical-align:middle;"><a href="#" class="pdf-quiz_6">Quiz_6</a></td>                  <td style="vertical-align:middle;">2015/11/11</td>				              
			</tbody>
			<tbody>			  			                    
				<td style="vertical-align:middle;">第七次小考</td>				                    <td style="vertical-align:middle;"><a href="#" class="pdf-quiz_7">Quiz_7</a></td>                  <td style="vertical-align:middle;">2015/12/02</td>				              
			</tbody>
			<tbody>			  			                    
				<td style="vertical-align:middle;">第八次小考</td>				                    <td style="vertical-align:middle;"><a href="#" class="pdf-quiz_8">Quiz_8</a></td>                  <td style="vertical-align:middle;">2015/12/11</td>				              
			</tbody>
			<tbody>			  			                    
				<td style="vertical-align:middle;">第九次小考</td>				                    <td style="vertical-align:middle;"><a href="#" class="pdf-quiz_9">Quiz_9</a></td>                  <td style="vertical-align:middle;">2015/12/16</td>				              
			</tbody>
			
			註解結束-->
			</div> 
		
		
		<!--其餘頁面GoogleTable顯示部份設定-->
			<div id="table-responsive-05" style="display:none;"><!--發問紀錄-->
				<iframe width="100%" height="800" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTDBhlvd_Id2h-GUQWLZbhDNqSp6BSMvISB48h6kc8nAV5k5qsXaRprnxOJiBvKe9iFjW6Fbw53ha4r/pubhtml?widget=true&amp;headers=false"></iframe>
			</div>
			<div id="table-responsive-06" style="display:none;">
				<iframe width="100%" height="800" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQslld3Mx63WQXUkXmk4O5zg55kI5pqxhcWg95vUbmSmdhR25DQRup2gbe6HvDkiKFzN6rzksRVWhag/pubhtml?widget=true&amp;headers=false"></iframe>
			</div>
			<div id="table-responsive-07" style="display:none;"><!--補強-->
				<iframe width="100%" height="800"src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQrmm9CVNxdmiZEuwvLoOnWdZ_S-u0ejnC4ecViQn30cp0kYyLemGJ6__caqgBTePB58r41qW2TB4PI/pubhtml?widget=true&amp;headers=false"></iframe>
			</div>
			<div id="table-responsive-08" style="display:none;">
				<iframe width="100%" height="800" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vT5C_Ul3EmC6LMLYdpoNWcvGUacIdNbAYEilmwXPnPyV3P2N6AZTCFwaNr7Vg3_b9S1VKTHd2ycFDOo/pubhtml?widget=true&amp;headers=false"></iframe>
			</div>
			<div id="table-responsive-09" style="display:none;"><!--小考成績查詢-->
				<iframe width="100%" height="800" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTRoTHJZnFXByoUA0Y174HL-kKhdM9kKoz6S0eTZJOoGGTumXchPtK7d1tOmFxqFeaIgR75JuR-NGRs/pubhtml?widget=true&amp;headers=false"></iframe>
			</div>
			<div id="table-responsive-10" style="display:none;">
				<iframe width="100%" height="800" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQ_lD_CGV4KLJDVFOiGzJZanJGaUr1EIs7EE9ftzjGUJW6TxEYxUxLJkqdQ9WMzBb_jyqQ8uSXnwxdA/pubhtml?widget=true&amp;headers=false"></iframe>
			</div>			
			<div id="table-responsive-12" style="display:none;"><!--程式練習狀況-->
			<iframe width="100%" height="800" src="https://docs.google.com/spreadsheets/d/1n6ZsfqLDKJ6I20rC35CaGjuno9idj42sKperWHgrQm0/pubhtml?gid=1402978687&amp;single=true&amp;widget=true&amp;headers=false"></iframe>				
			</div>
        
			<!--<div id="table-responsive-13" style="display:none;">
			<iframe width="100%" height="800" src="https://docs.google.com/spreadsheets/d/1n6ZsfqLDKJ6I20rC35CaGjuno9idj42sKperWHgrQm0/pubhtml?gid=1415003753&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
			</div>-->
			
			<div id="table-responsive-14" style="display:none;"><!--總成績-->
			<iframe width="100%" height="800" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSZiswNYdtHKD29xIU427nTYlf159kpkB-jB5PVtK5DdvIJ0FjsXgNYduhsl0X6GR0UHDzI1MiyI3Ao/pubhtml?widget=true&amp;headers=false"></iframe>
			</div>
			
			<div id="table-responsive-15" style="display:none;">
			<iframe width="100%" height="800" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vR7N4biH15IbS58XyVYqWgUwSMdZleGd4kVGTEhtQO0UHUalgfjbo_U3dPKrxBao04g4KtX13C1w8Ql/pubhtml?widget=true&amp;headers=false"></iframe>
			</div>
           <table class="table table-striped" id="table-responsive-11" style="display:none;">
              <thead>  
                       <tr>  
         	             <!-- <th class="title-font">週次</th> --> 
	                     <th class="title-font">名稱</th>
                	     <th class="title-font">解答</th>  
       		             <th class="title-font">上傳日期</th> 
                      </tr>
              </thead>

              <tbody>
    <tr>
                      <td style="vertical-align:middle;">2010演算法期中考</td>
                         <td style="vertical-align:middle;"><a href="https://goo.gl/BYZRhj" target="_blank">2010期中考</a></td>
                         <td style="vertical-align:middle;">2017/9/15</td>
                    </tr>
    <tr>
                      <td style="vertical-align:middle;">2010演算法期末考</td>
                         <td style="vertical-align:middle;"><a href="https://goo.gl/z8ceRK" target="_blank">2010期末考</a></td>
                         <td style="vertical-align:middle;">2017/9/15</td>
                    </tr>
		<tr>
   	             <td style="vertical-align:middle;">2011演算法期中考</td>
                     <td style="vertical-align:middle;"><a href="https://goo.gl/ogdQJ1" target="_blank">2011期中考</a></td>
                     <td style="vertical-align:middle;">2017/9/15</td>
                </tr>
		<tr>
                     <td style="vertical-align:middle;">2011演算法期末考</td>
                     <td style="vertical-align:middle;"><a href="https://goo.gl/3e3At9" target="_blank">2011期末考</a></td>
                     <td style="vertical-align:middle;">2017/9/15</td>
                </tr>
		<tr>
                   <td style="vertical-align:middle;">2012演算法期中考</td>
                   <td style="vertical-align:middle;"><a href="https://goo.gl/B91V6g" target="_blank">2012期中考</a></td>
                   <td style="vertical-align:middle;">2017/9/15</td>
                </tr>
    <tr>
                  <td style="vertical-align:middle;">2012演算法期末考</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/TcpRg6" target="_blank">2012期末考</a></td>
                  <td style="vertical-align:middle;">2017/9/15</td>
             </tr>
		<tr>
                   <td style="vertical-align:middle;">2013演算法期中考</td>
                   <td style="vertical-align:middle;"><a href="https://goo.gl/KgM5Ah" target="_blank">2013期中考</a></td>
                   <td style="vertical-align:middle;">2017/9/16</td>
                </tr>
		<tr>
                   <td style="vertical-align:middle;">2013演算法期末考</td>
                   <td style="vertical-align:middle;"><a href="https://goo.gl/VBieXX" target="_blank">2013期末考</a></td>
                   <td style="vertical-align:middle;">2017/9/16</td>
                </tr>
    <tr>
                  <td style="vertical-align:middle;">2013演算法期末考</td>
                  <td style="vertical-align:middle;"><a href="https://goo.gl/VBieXX" target="_blank">2013期末考</a></td>
                  <td style="vertical-align:middle;">2017/9/16</td>
               </tr>
	    </tbody>
           </table>
          </div>
          
        </div>
      </div>
    </div>

    <!-- Bootstrap core JavaScript
    ================================================== -->
    <!-- Placed at the end of the document so the pages load faster -->
    <script src="./lib/js/jquery.1.11.1.min.js"></script>
    <script src="./dist/js/bootstrap.min.js"></script>
    <script src="./assets/js/docs.min.js"></script>
    <!-- IE10 viewport hack for Surface/desktop Windows 8 bug -->
    <script src="./assets/js/ie10-viewport-bug-workaround.js"></script>
  </body>
</html>
