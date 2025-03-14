**衛星データから画像を読み込み、NDVIを算出したり、時系列予測を行うアプリケーションです。チャットボットに聞くこともできます。**<br>

仮想環境を構築したのちに以下のコマンドを実施してください<br>
python -m venv venv <br>
source venv/bin/activate # macOS, Linux <br>
venv\Scripts\activate # Windows <br>
pip install -r backend/requirements.txt <br>

.envファイルを作成し、その中に <br>
***gemini_api***<br>
GOOGLE_API_KEY="" <br>
***sentinel-hub_api***<br>
SH_CLIENT_ID="" <br>
SH_CLIENT_SECRET="" <br>
***weather.com_api***<br>
WEATHER_API_KEY=""<br>
を入力してください

**以下がこのプログラムの構成内容です**
agristar/<br>
├── app/<br>
│   ├── __init__.py<br>
│   ├── config.py<br>
│   ├── models/<br>
│   │   └── __init__.py<br>
│   ├── routes/<br>
│   │   ├── __init__.py<br>
│   │   ├── main_routes.py<br>
│   │   ├── map_routes.py<br>
│   │   └── chatbot_routes.py<br>
│   ├── services/<br>
│   │   ├── __init__.py<br>
│   │   └── satellite_service.py<br>
│   ├── static/<br>
│   │   ├── css/<br>
│   │   │   ├── main.css<br>
│   │   │   └── map.css<br>
│   │   ├── js/<br>
│   │   │   ├── main.js<br>
│   │   │   ├── map.js<br>
│   │   │   └── chatbot.js<br>
│   │   └── images/<br>
│   ├── templates/<br>
│   │   ├── base.html<br>
│   │   ├── index.html<br>
│   │   ├── map.html<br>
│   │   └── chatbot.html<br>
├── chatbot.py  # 既存のチャットボット実装<br>
├── run.py<br>
└── requirements.txt<br>