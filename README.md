# chat
let chat1 = this.props.chathistory.map(
            function(item, i){
                return item.sender?
                    <div key={i} className="d-flex justify-content-start mb-4">
                        <div className="img_cont_msg">
                            <img src="https://static.turbosquid.com/Preview/001292/481/WV/_D.jpg" className="rounded-circle user_img_msg"/>
                        </div>
                        <div className="msg_cotainer">
                        {"You: "+item.message}
                            <span className="msg_time">8:40 AM, Today</span>
                        </div>
                    </div>
                : 
                    // eslint-disable-next-line no-unreachable
                    <div key={i} className="d-flex justify-content-end mb-4">
								<div className="msg_cotainer_send">
                                {"Bot: "+item.text}
									<span className="msg_time_send">8:55 AM, Today</span>
								</div>
								<div className="img_cont_msg">
							        <img src="https://sun9-33.userapi.com/c540100/v540100324/4d824/GlVv9a61NnE.jpg" className="rounded-circle user_img_msg" />
								</div>
							</div>
            }
        )
	
	
	

<div className=" chat">
					<div className="card">
						<div className="card-header msg_head">
							<div className="d-flex bd-highlight">
								<div className="img_cont">
									<img src="https://static.turbosquid.com/Preview/001292/481/WV/_D.jpg" className="rounded-circle user_img"/>
									<span className="online_icon"></span>
								</div>
								<div className="user_info">
									<span>Chat with Khalid</span>
									<p>1767 Messages</p>
								</div>
							</div>
						</div>
						<div className="card-body msg_card_body">
                            {chat}
						</div>
						<div className="card-footer">
							<div className="input-group">
								<div className="input-group-append">
									<span className="input-group-text attach_btn"><i className="fas fa-paperclip"></i></span>
								</div>
								<textarea id="usrInput" name="" className="form-control type_msg" placeholder="Type your message..."></textarea>
                                
								<div className="input-group-append" onClick={this.sendMessage}>
									<span className="input-group-text send_btn"><i className="fas fa-location-arrow"><ion-icon name="send"></ion-icon></i></span>
								</div>
							</div>
						</div>
					</div>
		</div>
    
    ///////////////////////////////////////css//////////////////////////////
    .chat{
    margin-top: auto;
    margin-bottom: auto;
    position: fixed;
    bottom: 10px;
    right: 10px;
   
}
.card{
    height: 400px;
    width: 300px;
    border-radius: 15px !important;
    background-color: rgba(0,0,0,0.4) !important;
}
.contacts_body{
    padding:  0.75rem 0 !important;
    overflow-y: auto;
    white-space: nowrap;
}
.msg_card_body{
    overflow-y: auto;
}
.card-header{
    border-radius: 15px 15px 0 0 !important;
    border-bottom: 0 !important;
}
.card-footer{
border-radius: 0 0 15px 15px !important;
    border-top: 0 !important;
}
.container{
    align-content: center;
}
.search{
    border-radius: 15px 0 0 15px !important;
    background-color: rgba(0,0,0,0.3) !important;
    border:0 !important;
    color:white !important;
}
.search:focus{
     box-shadow:none !important;
   outline:0px !important;
}
.type_msg{
    background-color: rgba(0,0,0,0.3) !important;
    border:0 !important;
    color:white !important;
    height: 60px !important;
    overflow-y: auto;
}
    .type_msg:focus{
     box-shadow:none !important;
   outline:0px !important;
}
.attach_btn{
border-radius: 15px 0 0 15px !important;
background-color: rgba(0,0,0,0.3) !important;
    border:0 !important;
    color: white !important;
    cursor: pointer;
}
.send_btn{
border-radius: 0 15px 15px 0 !important;
background-color: rgba(0,0,0,0.3) !important;
    border:0 !important;
    color: white !important;
    cursor: pointer;
}
.search_btn{
    border-radius: 0 15px 15px 0 !important;
    background-color: rgba(0,0,0,0.3) !important;
    border:0 !important;
    color: white !important;
    cursor: pointer;
}
.contacts{
    list-style: none;
    padding: 0;
}
.contacts li{
    width: 100% !important;
    padding: 5px 10px;
    margin-bottom: 15px !important;
}
.active{
    background-color: rgba(0,0,0,0.3);
}
.user_img{
    height: 70px;
    width: 70px;
    border:1.5px solid #f5f6fa;

}
.user_img_msg{
    height: 40px;
    width: 40px;
    border:1.5px solid #f5f6fa;

}
.img_cont{
    position: relative;
    height: 70px;
    width: 70px;
}
.img_cont_msg{
    height: 40px;
    width: 40px;
}
.online_icon{
position: absolute;
height: 15px;
width:15px;
background-color: #4cd137;
border-radius: 50%;
bottom: 0.2em;
right: 0.4em;
border:1.5px solid white;
}
.offline{
background-color: #c23616 !important;
}
.user_info{
margin-top: auto;
margin-bottom: auto;
margin-left: 15px;
}
.user_info span{
font-size: 20px;
color: white;
}
.user_info p{
font-size: 10px;
color: rgba(255,255,255,0.6);
}
.video_cam{
margin-left: 50px;
margin-top: 5px;
}
.video_cam span{
color: white;
font-size: 20px;
cursor: pointer;
margin-right: 20px;
}
.msg_cotainer{
margin-top: auto;
margin-bottom: auto;
margin-left: 10px;
border-radius: 25px;
background-color: #82ccdd;
padding: 10px;
position: relative;
}
.msg_cotainer_send{
margin-top: auto;
margin-bottom: auto;
margin-right: 10px;
border-radius: 25px;
background-color: #78e08f;
padding: 10px;
position: relative;
}
.msg_time{
position: absolute;
left: 0;
bottom: -15px;
color: rgba(255,255,255,0.5);
font-size: 10px;
}
.msg_time_send{
position: absolute;
right:0;
bottom: -15px;
color: rgba(255,255,255,0.5);
font-size: 10px;
}
.msg_head{
position: relative;
}
#action_menu_btn{
position: absolute;
right: 10px;
top: 10px;
color: white;
cursor: pointer;
font-size: 20px;
}
.action_menu{
z-index: 1;
position: absolute;
padding: 15px 0;
background-color: rgba(0,0,0,0.5);
color: white;
border-radius: 15px;
top: 30px;
right: 15px;
display: none;
}
.action_menu ul{
list-style: none;
padding: 0;
margin: 0;
}
.action_menu ul li{
width: 100%;
padding: 10px 15px;
margin-bottom: 5px;
}
.action_menu ul li i{
padding-right: 10px;

}
.action_menu ul li:hover{
cursor: pointer;
background-color: rgba(0,0,0,0.2);
}
@media(max-width: 576px){
.contacts_card{
margin-bottom: 15px !important;
}
}
