---
title: "电影资源HTML"
excerpt: ""
header:
  image: /assets/images/
  teaser: assets/images/pika.gif

---
<html lang="zh-cn">

    <head>
        <meta charset="UTF-8">
        <title>My web work</title>
        <style type="text/css" content="text/html;charser=gb2312">
		 * {
            padding: 0;
            margin: 0;
        }

        html,
        body {
            height: 100%;
        }

        #container {
            width: 0 auto;
            margin: 0 auto;
            height: 10%;
        }

        #container div {
            height: 100%;
        }

        .col25 {
            width: 25%;
            background: lightgreen;
            float: left;
        }

        .col50 {
            width: 50%;
            background: lightblue;
            float: left;
        }

        .col75 {
            width: 75%;
            background: lightyellow;
            float: left;
        }
            * {
                padding: 0;
                margin: 0;
                list-style: none;
            }
            
            html,
            body {
                height: 100%;
				margin: 0;
				padding: 0
            }
            nav  {
				display: flex;
				min-height: 0 auto;
			}
			a  {
				font-family: sans-serif;
				color: #fff;
				text-indent: 1rem;
				
				display: inline-flex;
				flex: 1 1 20%;
				align-self: stretch;
				align-items: center;
				transition: box-shadow 1s;
				text-decoration: none;
			}
			a + a {
				border-left: 0 auto solid #aaa;
			}
			a:hover {
				box-shadow: inset 0 -10px 0 #CC3232;
			}
            #menu {
                width: 0 auto;
                margin: 0 auto;
                display: flex;  /*当前块为弹性盒*/
            }
            #menu li{
                flex: auto;  /*弹性盒中的单项*/
                float: left;
            }
            #menu li a{
                display:block;
                height: 0 auto;
                line-height: 0 auto;
                border:1px solid cornflowerblue;
                margin-right: 0 auto;
                text-decoration: none;
                text-align: center;
				background-color: #ccc
            }
        </style>
    

		<body>
			<ul id="menu">
				<li><a href="http://www.btbtt88.com/forum-index-fid-1-typeid1-1-typeid2-0-typeid3-0-typeid4-0.htm" class="item">European and American films</a></li>
				<li><a href="http://www.btbtt88.com/forum-index-fid-1-typeid1-0-typeid2-246-typeid3-0-typeid4-0.htm" class="item">Plot film</a></li>
				<li><a href="http://www.btbtt88.com/forum-index-fid-1-typeid1-3-typeid2-0-typeid3-0-typeid4-0.htm" class="item">Hongkong film</a></li>
				<li><a href="http://www.btbtt88.com/forum-index-fid-1-typeid1-9-typeid2-0-typeid3-0-typeid4-0.htm" class="item">Continental film</a></li>
				<li><a href="http://www.btbtt88.com/forum-index-fid-9.htm" class="item">Welfare Film</a></li>
				<li><a href="http://www.gao4.com/page2/b/" class="item">Don't touch me</a></li>
				
			</ul>
			<div id="container">
				<div class="col25">
					Newest
					<li><a href="http://www.btbtt88.com/thread-index-fid-1-tid-13216.htm" class="item">Justice League: Injustice for All</a></li>
					
				</div>
				<div class="col50">
					Classic film
					<li><a href="http://www.btbtt88.com/thread-index-fid-1-tid-7385.htm" class="item">The fantasy drifting of the young school</a></li>
				</div>

				<div class="col25">
					Welfare Film
					<li><a href="http://www.btbtt88.com/thread-index-fid-9-tid-13334.htm" class="item">The girl next door</a></li>
				</div>
			</div>
		</body>
	</head>
</html>