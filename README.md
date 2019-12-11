1.  Install Elasticsearch Cài elasticsearch 7.3.1 :
    https://www.elastic.co/downloads/past-releases/elasticsearch-7-3-1
    Dowload Vietnamese Analysis Plugin for Elasticsearch :
    https://github.com/duydo/elasticsearch-analysis-vietnamese
    bin\elasticsearch-plugin install
    file:///C:/path\_to/elasticsearch-analysis-vietnamese-7.3.1.zip Run
    elasticsearch

2.  Setup Project git clone https://github.com/ozil-thang/BookSearch.git
    cd BookSearch conda create --name book\_search\_env conda activate
    book\_search\_env conda install pip pip install -r requirements.txt

Open file process\_crawl\_data.py line 22 change n for number book to
index (default: 1000 / \~9700), if you want index all book (\~ 9700)
delete line 26

python process\_crawl\_data.py python index\_data\_elasticsearch.py
\#(1000 book \~ 10 minutes) python app.py
