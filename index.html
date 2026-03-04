# hand-size
手の大きさ比較ツール
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta charset="UTF-8">
    <title>手の大きさ比較ツール</title>
    <style>
        body { font-family: 'Helvetica Neue', Arial, sans-serif; text-align: center; background: #fdf6e3; padding: 10px; color: #333; margin: 0; }
        .container { max-width: 700px; margin: 20px auto; background: white; padding: 20px; border-radius: 15px; box-shadow: 0 10px 25px rgba(0,0,0,0.05); }
        h1 { font-size: 1.5rem; margin-bottom: 10px; color: #444; }
        .description { font-size: 13px; color: #666; margin-bottom: 20px; line-height: 1.6; }
        
        .display-area { 
            position: relative; height: 450px; border: 2px solid #eee; margin-top: 20px; 
            display: flex; justify-content: center; align-items: flex-end; overflow: hidden; 
            background-color: #fff; border-radius: 10px;
        }

        #zoom-container {
            position: relative; width: 100%; height: 100%;
            display: flex; justify-content: center; align-items: flex-end;
            transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            transform-origin: bottom center;
        }
        
        .hand-wrapper { 
            position: absolute; 
            bottom: 20px; /* 手首の基準位置 */
            left: 50%; 
            transform: translateX(-50%); 
            display: flex; 
            flex-direction: column; 
            align-items: center; 
            transition: z-index 0.3s; 
        }

        .hand-svg-container { 
            transform-origin: bottom center; 
            transition: 0.5s cubic-bezier(0.4, 0, 0.2, 1); 
            will-change: transform; 
        }

        .label-tag { 
            position: absolute;
            /* 下（手首）からの距離をJSで制御するため、bottom基準にする */
            bottom: 0;
            font-size: 14px; 
            font-weight: bold; 
            white-space: nowrap; 
            background: rgba(255,255,255,0.9); 
            padding: 4px 12px; 
            border-radius: 20px; 
            box-shadow: 0 2px 5px rgba(0,0,0,0.1); 
            z-index: 10; 
            transition: 0.5s cubic-bezier(0.4, 0, 0.2, 1); 
        }

        .controls { display: flex; flex-direction: column; gap: 12px; }
        .input-group { display: flex; align-items: center; justify-content: center; flex-wrap: wrap; gap: 8px; padding: 15px; border-radius: 12px; }
        .group-a { background: #fff0e0; border: 1px solid #ffe0c0; }
        .group-b { background: #e0f0ff; border: 1px solid #c0e0ff; }
        
        input, select { padding: 8px; border: 1px solid #ccc; border-radius: 6px; font-size: 14px; }
        .num-input { width: 65px; }
        .hint { font-size: 10px; color: #888; display: block; margin-bottom: 2px; }
        .color-picker { width: 35px; height: 35px; border: none; background: none; cursor: pointer; padding: 0; }
        .btn-front { padding: 6px 12px; cursor: pointer; border-radius: 20px; border: 1px solid #999; background: #fff; font-size: 12px; font-weight: bold; }
        .btn-front:hover { background: #f0f0f0; }

        .share-area { margin-top: 20px; border-top: 1px dashed #ccc; padding-top: 20px; }
        .btn-share { background: #000; color: #fff; border: none; padding: 10px 24px; border-radius: 25px; cursor: pointer; font-weight: bold; font-size: 14px; }
        .license-text { margin-top: 25px; font-size: 10px; color: #aaa; line-height: 1.6; }
    </style>
</head>
<body>

<div class="container">
    <h1>✋手の大きさ比較ツール</h1> 
    <p class="description">
       性別と身長から手の大きさを推測できます。<br>
       実際の数値を入力して比較することもできます。<br>
        <small>※初期値は各性別の平均値です。<br>
            個人差があるため、数値はあくまで目安としてお楽しみください。<br>
            （出典：産総研人体寸法データベース等を参考にした推測値）</small>
    </p>

    <div class="controls">
        <div class="input-group group-a">
            <strong>A</strong>
            <input type="text" id="nameInputA" placeholder="名前A" oninput="update()">
            <select id="genderA" onchange="calcFromHeight('A')">
                <option value="male">男</option>
                <option value="female">女</option>
            </select>
            <div><span class="hint">身長(cm)</span><input type="number" id="heightA" class="num-input" value="171.5" oninput="calcFromHeight('A')"></div>
            <div style="border-left: 1px solid #ccc; padding-left: 8px;"><span class="hint">手首〜中指先(cm)※優先</span><input type="number" id="handA" class="num-input" value="18.5" step="0.1" oninput="calcFromHand('A')"></div>
            <input type="color" id="colorA" class="color-picker" value="#ffcc99" oninput="update()">
            <button class="btn-front" onclick="bringToFront('A')">前へ</button>
        </div>

        <div class="input-group group-b">
            <strong>B</strong>
            <input type="text" id="nameInputB" placeholder="名前B" oninput="update()">
            <select id="genderB" onchange="calcFromHeight('B')">
                <option value="male">男</option>
                <option value="female" selected>女</option>
            </select>
            <div><span class="hint">身長(cm)</span><input type="number" id="heightB" class="num-input" value="158.0" oninput="calcFromHeight('B')"></div>
            <div style="border-left: 1px solid #ccc; padding-left: 8px;"><span class="hint">手首〜中指先(cm)※優先</span><input type="number" id="handB" class="num-input" value="16.6" step="0.1" oninput="calcFromHand('B')"></div>
            <input type="color" id="colorB" class="color-picker" value="#ffad60" oninput="update()">
            <button class="btn-front" onclick="bringToFront('B')">前へ</button>
        </div>
    </div>
    
    <div class="display-area">
        <div id="zoom-container">
            <div id="wrapperA" class="hand-wrapper" style="z-index: 1;">
                <div id="labelA" class="label-tag"></div>
                <div class="hand-svg-container" id="svgContainerA">
                    <svg width="250" height="300" viewBox="0 0 25.922 25.922">
                        <path id="shapeA" opacity="0.7" d="M3.308,16.35c1.46-0.876,2.288,0.117,3.883,0.861c1.371,0.64,2.899,0.65,3.033-0.153 c0.216-1.297,0.169-1.916,0.169-3.679c0-1.401-0.442-4.576-0.791-6.975c-0.42-2.887-0.566-4.577,0.851-4.71 c1.36-0.128,1.428,0.639,1.945,4.56c0.396,3.006,1.023,5.121,1.336,5.059c0.313-0.062-0.152-2.786-0.266-5.563 C13.265,0.781,13.531,0,14.781,0c1.077,0,1.312,0.703,1.452,5.75c0.073,2.625,0.359,5.358,0.581,5.358 c0.334,0,0.599-2.563,0.548-5.341c-0.097-5.194,0.817-4.802,1.367-4.802c0.542,0,1.489,0.153,1.459,5.106 c-0.019,2.896,0,5.396,0.547,5.396c0.244,0,0.638-2.334,0.638-4.606c0-3.8,0.729-3.8,1.308-3.8c0.577,0,0.881,0.7,0.911,4.499 c0.025,3.028-0.327,7.291-0.327,9.875c0,6.289-2.041,6.355-2.041,8.487h-8.541c-0.251-0.604-0.832-0.958-2.231-2.387 c-1.411-1.441-4.606-4.198-7.125-4.74C1.641,18.433,2.407,16.891,3.308,16.35z"/>
                    </svg>
                </div>
            </div>
            <div id="wrapperB" class="hand-wrapper" style="z-index: 2;">
                <div id="labelB" class="label-tag"></div>
                <div class="hand-svg-container" id="svgContainerB">
                    <svg width="250" height="300" viewBox="0 0 25.922 25.922">
                        <path id="shapeB" opacity="0.7" d="M3.308,16.35c1.46-0.876,2.288,0.117,3.883,0.861c1.371,0.64,2.899,0.65,3.033-0.153 c0.216-1.297,0.169-1.916,0.169-3.679c0-1.401-0.442-4.576-0.791-6.975c-0.42-2.887-0.566-4.577,0.851-4.71 c1.36-0.128,1.428,0.639,1.945,4.56c0.396,3.006,1.023,5.121,1.336,5.059c0.313-0.062-0.152-2.786-0.266-5.563 C13.265,0.781,13.531,0,14.781,0c1.077,0,1.312,0.703,1.452,5.75c0.073,2.625,0.359,5.358,0.581,5.358 c0.334,0,0.599-2.563,0.548-5.341c-0.097-5.194,0.817-4.802,1.367-4.802c0.542,0,1.489,0.153,1.459,5.106 c-0.019,2.896,0,5.396,0.547,5.396c0.244,0,0.638-2.334,0.638-4.606c0-3.8,0.729-3.8,1.308-3.8c0.577,0,0.881,0.7,0.911,4.499 c0.025,3.028-0.327,7.291-0.327,9.875c0,6.289-2.041,6.355-2.041,8.487h-8.541c-0.251-0.604-0.832-0.958-2.231-2.387 c-1.411-1.441-4.606-4.198-7.125-4.74C1.641,18.433,2.407,16.891,3.308,16.35z"/>
                    </svg>
                </div>
            </div>
        </div>
    </div>

    <div class="share-area">
        <button class="btn-share" onclick="shareOnX()">𝕏 で結果をシェアする</button>
        <div class="license-text">
            スクショ投稿や加工、トレース等はご自由にお楽しみください。<br>
            ※営利目的や商用利用はご遠慮ください。
        </div>
    </div>
</div>

<script>
    function calcFromHeight(target) {
        const h = parseFloat(document.getElementById('height' + target).value);
        const gender = document.getElementById('gender' + target).value;
        if (!h) return;
        let result = (gender === 'male') ? (h * 0.096 + 2.0).toFixed(1) : (h * 0.088 + 2.7).toFixed(1);
        document.getElementById('hand' + target).value = result;
        update(); 
    }

    function calcFromHand(target) {
        const hand = parseFloat(document.getElementById('hand' + target).value);
        const gender = document.getElementById('gender' + target).value;
        if (!hand) return;
        let height = (gender === 'male') ? ((hand - 2.0) / 0.096).toFixed(1) : ((hand - 2.7) / 0.088).toFixed(1);
        document.getElementById('height' + target).value = height;
        update();
    }
    
    function bringToFront(target) {
        document.getElementById('wrapperA').style.zIndex = (target === 'A') ? "10" : "1";
        document.getElementById('wrapperB').style.zIndex = (target === 'B') ? "10" : "1";
    }

    function update() {
        const nameA = document.getElementById('nameInputA').value || "名前A";
        const nameB = document.getElementById('nameInputB').value || "名前B";
        const handA = parseFloat(document.getElementById('handA').value) || 0;
        const handB = parseFloat(document.getElementById('handB').value) || 0;
        
        document.getElementById('labelA').innerText = `${nameA} (${handA}cm)`;
        document.getElementById('labelB').innerText = `${nameB} (${handB}cm)`;
        
        document.getElementById('shapeA').setAttribute('fill', document.getElementById('colorA').value);
        document.getElementById('shapeB').setAttribute('fill', document.getElementById('colorB').value);

        const baseSize = 20; // 基準となる手の長さ
        const scaleA = handA / baseSize;
        const scaleB = handB / baseSize;

        // 手の拡大縮小
        document.getElementById('svgContainerA').style.transform = `scale(${scaleA})`;
        document.getElementById('svgContainerB').style.transform = `scale(${scaleB})`;

        // ラベル位置調整（手首から指先までのピクセル数に合わせる）
        // SVGの元の高さ300pxにスケールを掛け、さらに少し余白(10px)を足す
        const labelPosA = (300 * scaleA) + 10;
        const labelPosB = (300 * scaleB) + 10;
        document.getElementById('labelA').style.bottom = `${labelPosA}px`;
        document.getElementById('labelB').style.bottom = `${labelPosB}px`;

        // 全体のズーム調整（枠からはみ出さないように）
        const maxHand = Math.max(handA, handB);
        const zoomThreshold = 22; 
        let zoomScale = 1;
        
        if (maxHand > zoomThreshold) {
            zoomScale = zoomThreshold / maxHand;
        }
        document.getElementById('zoom-container').style.transform = `scale(${zoomScale})`;
    }

    function shareOnX() {
        const nameA = document.getElementById('nameInputA').value || "名前A";
        const nameB = document.getElementById('nameInputB').value || "名前B";
        const handA = document.getElementById('handA').value;
        const handB = document.getElementById('handB').value;
        const text = encodeURIComponent(`${nameA}(${handA}cm)と${nameB}(${handB}cm)の手の大きさを比較しました！\n#手の大きさ比較ツール\n`);
        const url = encodeURIComponent(window.location.href);
        window.open(`https://twitter.com/intent/tweet?text=${text}&url=${url}`, '_blank');
    }

    window.onload = update;
</script>
</body>
</html>
