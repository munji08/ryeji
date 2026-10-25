<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>신류진 아이폰 시뮬레이터</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            user-select: none;
            -webkit-user-select: none;
            font-family: -apple-system, BlinkMacSystemFont, "SF Pro Text", "SF Pro Display", "Helvetica Neue", Arial, sans-serif;
        }

        body {
            background-color: #0f1115;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            overflow: hidden;
            color: #fff;
        }

        /* 아이폰 프레임 */
        .iphone-container {
            width: 390px;
            height: 844px;
            background-color: #000;
            border-radius: 50px;
            box-shadow: 0 0 0 12px #2b2b2e, 0 0 0 13px #1a1a1a, 0 30px 60px rgba(0, 0, 0, 0.8);
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }

        /* 다이내믹 아일랜드 & 상단 바 */
        .status-bar {
            height: 47px;
            width: 100%;
            padding: 0 24px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: absolute;
            top: 0;
            left: 0;
            z-index: 1000;
            font-size: 14px;
            font-weight: 600;
        }

        .dynamic-island {
            position: absolute;
            top: 10px;
            left: 50%;
            transform: translateX(-50%);
            width: 120px;
            height: 35px;
            background-color: #000;
            border-radius: 20px;
            z-index: 1001;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .status-icons {
            display: flex;
            align-items: center;
            gap: 6px;
            font-size: 12px;
        }

        /* 화면 공통 */
        .screen {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #000000;
            display: flex;
            flex-direction: column;
            transition: opacity 0.3s ease, transform 0.3s ease;
            opacity: 0;
            pointer-events: none;
            z-index: 1;
        }

        .screen.active {
            opacity: 1;
            pointer-events: auto;
            z-index: 10;
        }

        /* 1. 잠금화면 */
        #lock-screen {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            padding: 60px 20px 40px;
            background-color: #000000;
            touch-action: none;
        }

        .lock-clock {
            font-size: 80px;
            font-weight: 200;
            letter-spacing: -2px;
            margin-top: 20px;
            line-height: 1;
        }

        .lock-date {
            font-size: 18px;
            font-weight: 500;
            color: rgba(255, 255, 255, 0.8);
            margin-top: 5px;
        }

        .swipe-hint {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
            color: rgba(255, 255, 255, 0.6);
            font-size: 14px;
            animation: pulse 2s infinite;
            cursor: pointer;
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.4; transform: translateY(0); }
            50% { opacity: 0.9; transform: translateY(-5px); }
        }

        /* 암호 입력 키패드 오버레이 */
        .passcode-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.85);
            backdrop-filter: blur(30px);
            -webkit-backdrop-filter: blur(30px);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            z-index: 20;
            transform: translateY(100%);
            transition: transform 0.4s cubic-bezier(0.1, 0.9, 0.2, 1);
        }

        .passcode-overlay.show {
            transform: translateY(0);
        }

        .passcode-title {
            font-size: 20px;
            font-weight: 500;
            margin-bottom: 20px;
        }

        .passcode-dots {
            display: flex;
            gap: 16px;
            margin-bottom: 40px;
        }

        .dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            border: 2px solid #fff;
            transition: background 0.2s;
        }

        .dot.filled {
            background-color: #fff;
        }

        .keypad {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px 25px;
        }

        .key-btn {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.15);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            font-size: 26px;
            font-weight: 400;
            cursor: pointer;
            transition: background 0.15s;
        }

        .key-btn:active {
            background: rgba(255, 255, 255, 0.4);
        }

        .key-sub {
            font-size: 9px;
            letter-spacing: 1px;
            margin-top: -2px;
            opacity: 0.8;
        }

        /* 2. 홈 화면 */
        #home-screen {
            background-color: #000000;
            padding: 80px 24px 40px;
            display: flex;
            flex-direction: column;
        }

        .folder-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 24px 20px;
        }

        .app-folder {
            background: rgba(40, 40, 40, 0.6);
            backdrop-filter: blur(15px);
            border-radius: 22px;
            padding: 12px;
            height: 140px;
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 8px;
            cursor: pointer;
            transition: transform 0.2s;
        }

        .app-folder:active {
            transform: scale(0.96);
        }

        .folder-icon {
            background: #333;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            overflow: hidden;
        }

        .folder-label {
            text-align: center;
            font-size: 12px;
            margin-top: 6px;
            color: #ddd;
        }

        /* 폴더 열림 팝업 */
        .folder-modal {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            z-index: 50;
            display: none;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .folder-modal.active {
            display: flex;
        }

        .folder-modal-content {
            background: rgba(50, 50, 50, 0.5);
            width: 320px;
            height: 320px;
            border-radius: 36px;
            padding: 24px;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            align-content: start;
        }

        .app-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            cursor: pointer;
        }

        .app-item-icon {
            width: 60px;
            height: 60px;
            border-radius: 14px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
        }

        .app-item-name {
            font-size: 11px;
            margin-top: 6px;
            color: #fff;
        }

        /* 3. 카카오톡 앱 */
        #kakao-app {
            background-color: #abc1d1;
            color: #000;
        }

        .app-header {
            height: 88px;
            padding-top: 40px;
            padding-left: 16px;
            padding-right: 16px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: #fff;
            border-bottom: 1px solid #e0e0e0;
        }

        .chat-list {
            flex: 1;
            background: #fff;
            overflow-y: auto;
        }

        .chat-item {
            display: flex;
            padding: 12px 16px;
            align-items: center;
            gap: 12px;
            border-bottom: 1px solid #f5f5f5;
            cursor: pointer;
        }

        .chat-avatar {
            width: 48px;
            height: 48px;
            border-radius: 18px;
            background: #ddd;
            overflow: hidden;
            flex-shrink: 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .chat-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .chat-info {
            flex: 1;
        }

        .chat-title {
            font-size: 15px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 4px;
        }

        .chat-badge {
            font-size: 11px;
            color: #888;
            font-weight: normal;
        }

        .chat-preview {
            font-size: 13px;
            color: #666;
            margin-top: 3px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            max-width: 200px;
        }

        .chat-room {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #abc1d1;
            z-index: 10;
            display: flex;
            flex-direction: column;
            transform: translateX(100%);
            transition: transform 0.3s ease;
        }

        .chat-room.active {
            transform: translateX(0);
        }

        .chat-room-header {
            height: 88px;
            padding-top: 40px;
            padding-left: 12px;
            padding-right: 16px;
            background: #a0b7c9;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .chat-messages {
            flex: 1;
            padding: 16px;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .msg-bubble {
            max-width: 70%;
            padding: 8px 12px;
            border-radius: 12px;
            font-size: 14px;
            line-height: 1.4;
            position: relative;
        }

        .msg-left {
            align-self: flex-start;
            background: #fff;
            color: #000;
            border-top-left-radius: 2px;
        }

        .msg-right {
            align-self: flex-end;
            background: #ffe600;
            color: #000;
            border-top-right-radius: 2px;
        }

        /* 4. 카메라 앱 */
        #camera-app {
            background-color: #000;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .camera-view {
            flex: 1;
            position: relative;
            background: #111;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            margin-top: 47px;
            border-radius: 20px;
        }

        .camera-view video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .camera-controls {
            height: 120px;
            display: flex;
            align-items: center;
            justify-content: space-around;
            padding-bottom: 20px;
        }

        .shutter-btn {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            border: 4px solid #fff;
            background: transparent;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .shutter-btn-inner {
            width: 56px;
            height: 56px;
            border-radius: 50%;
            background: #fff;
        }

        /* 홈 바 (Home Indicator) */
        .home-indicator {
            position: absolute;
            bottom: 8px;
            left: 50%;
            transform: translateX(-50%);
            width: 134px;
            height: 5px;
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 3px;
            z-index: 2000;
            cursor: pointer;
        }
    </style>
</head>
<body>

<div class="iphone-container">
    <!-- 다이내믹 아일랜드 & 상단 바 -->
    <div class="dynamic-island"></div>
    <div class="status-bar">
        <span>01:22</span>
        <div class="status-icons">
            <span>5G</span>
            <span>88%</span>
        </div>
    </div>

    <!-- 1. 잠금 화면 -->
    <div class="screen active" id="lock-screen">
        <div style="text-align: center;">
            <div class="lock-date">10월 26일 월요일</div>
            <div class="lock-clock">01:22</div>
        </div>

        <div class="swipe-hint" onclick="showPasscode()">
            <span>🔒</span>
            <span>위로 쓸어올려서 잠금 해제</span>
        </div>

        <!-- 암호 키패드 오버레이 -->
        <div class="passcode-overlay" id="passcode-overlay">
            <div class="passcode-title">암호 입력</div>
            <div class="passcode-dots">
                <div class="dot"></div>
                <div class="dot"></div>
                <div class="dot"></div>
                <div class="dot"></div>
            </div>
            <div class="keypad">
                <div class="key-btn" onclick="pressKey('1')">1</div>
                <div class="key-btn" onclick="pressKey('2')">2<span class="key-sub">ABC</span></div>
                <div class="key-btn" onclick="pressKey('3')">3<span class="key-sub">DEF</span></div>
                <div class="key-btn" onclick="pressKey('4')">4<span class="key-sub">GHI</span></div>
                <div class="key-btn" onclick="pressKey('5')">5<span class="key-sub">JKL</span></div>
                <div class="key-btn" onclick="pressKey('6')">6<span class="key-sub">MNO</span></div>
                <div class="key-btn" onclick="pressKey('7')">7<span class="key-sub">PQRS</span></div>
                <div class="key-btn" onclick="pressKey('8')">8<span class="key-sub">TUV</span></div>
                <div class="key-btn" onclick="pressKey('9')">9<span class="key-sub">WXYZ</span></div>
                <div></div>
                <div class="key-btn" onclick="pressKey('0')">0</div>
                <div class="key-btn" style="font-size: 14px; background: transparent;" onclick="hidePasscode()">취소</div>
            </div>
        </div>
    </div>

    <!-- 2. 홈 화면 -->
    <div class="screen" id="home-screen">
        <div class="folder-grid">
            <!-- 어플 폴더 1 -->
            <div>
                <div class="app-folder" onclick="openFolder('social')">
                    <div class="folder-icon" style="background:#fee500; color:#000;">💬</div>
                    <div class="folder-icon" style="background:#333;">📷</div>
                    <div class="folder-icon" style="background:#222;">🖼️</div>
                    <div class="folder-icon" style="background:#333;">📝</div>
                </div>
                <div class="folder-label">소셜 & 미디어</div>
            </div>

            <!-- 어플 폴더 2 -->
            <div>
                <div class="app-folder" onclick="openFolder('sys')">
                    <div class="folder-icon" style="background:#30d158;">📞</div>
                    <div class="folder-icon" style="background:#8e8e93;">⚙️</div>
                </div>
                <div class="folder-label">유틸리티</div>
            </div>
        </div>
    </div>

    <!-- 폴더 열림 팝업 -->
    <div class="folder-modal" id="folder-modal" onclick="closeFolder(event)">
        <div class="folder-modal-content" onclick="event.stopPropagation()">
            <div class="app-item" onclick="openApp('kakao')">
                <div class="app-item-icon" style="background: #fee500; color: #000;">💬</div>
                <div class="app-item-name">카카오톡</div>
            </div>
            <div class="app-item" onclick="openApp('camera')">
                <div class="app-item-icon" style="background: linear-gradient(135deg, #a1a8b0, #5a626a);">📷</div>
                <div class="app-item-name">카메라</div>
            </div>
            <div class="app-item" onclick="openApp('photos')">
                <div class="app-item-icon" style="background: #fff; color:#000;">🖼️</div>
                <div class="app-item-name">사진</div>
            </div>
            <div class="app-item" onclick="openApp('notes')">
                <div class="app-item-icon" style="background: #fbc02d; color:#fff;">📝</div>
                <div class="app-item-name">메모</div>
            </div>
        </div>
    </div>

    <!-- 3. 카카오톡 앱 -->
    <div class="screen" id="kakao-app">
        <div class="app-header">
            <span style="font-size: 20px; font-weight: bold;">채팅</span>
        </div>
        <div class="chat-list">
            <!-- 1. 황예지 언니 (2번 사진 프사) -->
            <div class="chat-item" onclick="openChat('yeji')">
                <div class="chat-avatar">
                    <img src="1000070277.jpg" alt="황예지" onerror="this.src='https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=100&auto=format&fit=crop'">
                </div>
                <div class="chat-info">
                    <div class="chat-title">황예지 언니</div>
                    <div class="chat-preview">류진아 오늘 연습실 몇시에 올 거야?</div>
                </div>
            </div>

            <!-- 2. ⭐️ITZY⭐️ (1번 실루엣 프사, 5명) -->
            <div class="chat-item" onclick="openChat('itzy')">
                <div class="chat-avatar">
                    <img src="1000070719.jpg" alt="ITZY" onerror="this.src='https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?w=100&auto=format&fit=crop'">
                </div>
                <div class="chat-info">
                    <div class="chat-title">⭐️ITZY⭐️ <span class="chat-badge">5</span></div>
                    <div class="chat-preview">유나: 단체 스케줄 공지 확인해주세요!</div>
                </div>
            </div>

            <!-- 3. 매니저님 -->
            <div class="chat-item" onclick="openChat('manager')">
                <div class="chat-avatar">
                    <img src="1000070719.jpg" alt="매니저" onerror="this.src='https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?w=100&auto=format&fit=crop'">
                </div>
                <div class="chat-info">
                    <div class="chat-title">매니저님</div>
                    <div class="chat-preview">류진씨 내일 픽업 시간 8시입니다.</div>
                </div>
            </div>

            <!-- 4. 지민언니 -->
            <div class="chat-item" onclick="openChat('jimin')">
                <div class="chat-avatar">
                    <img src="1000070719.jpg" alt="지민언니" onerror="this.src='https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?w=100&auto=format&fit=crop'">
                </div>
                <div class="chat-info">
                    <div class="chat-title">지민언니</div>
                    <div class="chat-preview">지난번에 말한 카페 위치 보냈어!</div>
                </div>
            </div>

            <!-- 5. 이채령 -->
            <div class="chat-item" onclick="openChat('chaeryeong')">
                <div class="chat-avatar">
                    <img src="1000070719.jpg" alt="이채령" onerror="this.src='https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?w=100&auto=format&fit=crop'">
                </div>
                <div class="chat-info">
                    <div class="chat-title">이채령</div>
                    <div class="chat-preview">언니 안무 영상 카톡으로 보내줄게!</div>
                </div>
            </div>
        </div>

        <!-- 채팅방 내부 -->
        <div class="chat-room" id="chat-room">
            <div class="chat-room-header">
                <span style="cursor: pointer; font-size: 18px;" onclick="closeChat()">❮</span>
                <span id="chat-room-title" style="font-weight: bold; font-size: 16px;">황예지 언니</span>
                <span></span>
            </div>
            <div class="chat-messages" id="chat-messages"></div>
        </div>
    </div>

    <!-- 4. 카메라 앱 -->
    <div class="screen" id="camera-app">
        <div class="camera-view">
            <video id="camera-video" autoplay playsinline muted></video>
        </div>
        <div class="camera-controls">
            <div style="width: 40px; height: 40px; background: #222; border-radius: 8px;"></div>
            <div class="shutter-btn" onclick="takePhoto()">
                <div class="shutter-btn-inner"></div>
            </div>
            <div style="width: 40px; height: 40px;"></div>
        </div>
    </div>

    <!-- 아이폰 하단 홈 바 -->
    <div class="home-indicator" onclick="goHome()"></div>
</div>

<script>
    let currentPasscode = "";
    const CORRECT_PASSCODE = "0526";

    // 스와이프 및 클릭 시 암호창 표시
    function showPasscode() {
        document.getElementById('passcode-overlay').classList.add('show');
    }

    function hidePasscode() {
        document.getElementById('passcode-overlay').classList.remove('show');
        currentPasscode = "";
        updateDots();
    }

    // 암호 입력 버튼
    function pressKey(num) {
        if (currentPasscode.length < 4) {
            currentPasscode += num;
            updateDots();

            if (currentPasscode.length === 4) {
                setTimeout(() => {
                    if (currentPasscode === CORRECT_PASSCODE) {
                        hidePasscode();
                        document.getElementById('lock-screen').classList.remove('active');
                        document.getElementById('home-screen').classList.add('active');
                    } else {
                        alert('암호가 올바르지 않습니다.');
                        currentPasscode = "";
                        updateDots();
                    }
                }, 200);
            }
        }
    }

    function updateDots() {
        const dots = document.querySelectorAll('.dot');
        dots.forEach((dot, idx) => {
            if (idx < currentPasscode.length) {
                dot.classList.add('filled');
            } else {
                dot.classList.remove('filled');
            }
        });
    }

    // 폴더 및 앱 관리
    function openFolder(name) {
        document.getElementById('folder-modal').classList.add('active');
    }

    function closeFolder(e) {
        document.getElementById('folder-modal').classList.remove('active');
    }

    function openApp(appId) {
        closeFolder();
        document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
        
        if (appId === 'kakao') {
            document.getElementById('kakao-app').classList.add('active');
        } else if (appId === 'camera') {
            document.getElementById('camera-app').classList.add('active');
            startCamera();
        }
    }

    function goHome() {
        document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
        document.getElementById('home-screen').classList.add('active');
        closeFolder();
        stopCamera();
    }

    // 채팅방 제어
    const chatData = {
        'yeji': {
            title: '황예지 언니',
            msgs: [
                { side: 'left', text: '류진아 오늘 연습실 몇시에 올 거야?' },
                { side: 'right', text: '나 6시쯤 도착할 것 같아 언니!' },
                { side: 'left', text: '오케이 오다가 아메리카노 하나만 부탁해 ☕' }
            ]
        },
        'itzy': {
            title: '⭐️ITZY⭐️ (5)',
            msgs: [
                { side: 'left', text: '유나: 언니들 오늘 단체 안무 영상 체크해주세요!' },
                { side: 'left', text: '채령: 확인 완료!' },
                { side: 'left', text: '리아: 나도 봤어 👍' }
            ]
        },
        'manager': {
            title: '매니저님',
            msgs: [
                { side: 'left', text: '류진씨 내일 픽업 시간 8시입니다.' },
                { side: 'right', text: '네 확인했습니다!' }
            ]
        },
        'jimin': {
            title: '지민언니',
            msgs: [
                { side: 'left', text: '지난번에 말한 카페 위치 보냈어!' }
            ]
        },
        'chaeryeong': {
            title: '이채령',
            msgs: [
                { side: 'left', text: '언니 안무 영상 카톡으로 보내줄게!' }
            ]
        }
    };

    function openChat(id) {
        const room = document.getElementById('chat-room');
        const title = document.getElementById('chat-room-title');
        const msgs = document.getElementById('chat-messages');

        const data = chatData[id];
        title.innerText = data.title;
        msgs.innerHTML = '';

        data.msgs.forEach(m => {
            const div = document.createElement('div');
            div.className = `msg-bubble msg-${m.side}`;
            div.innerText = m.text;
            msgs.appendChild(div);
        });

        room.classList.add('active');
    }

    function closeChat() {
        document.getElementById('chat-room').classList.remove('active');
    }

    // 카메라
    let mediaStream = null;
    async function startCamera() {
        try {
            mediaStream = await navigator.mediaDevices.getUserMedia({ video: true });
            document.getElementById('camera-video').srcObject = mediaStream;
        } catch (e) {
            console.log("카메라 접근 불가");
        }
    }

    function stopCamera() {
        if (mediaStream) {
            mediaStream.getTracks().forEach(track => track.stop());
            mediaStream = null;
        }
    }

    function takePhoto() {
        alert('📷 사진이 촬영되어 사진첩에 저장되었습니다!');
    }
</script>

</body>
</html>
