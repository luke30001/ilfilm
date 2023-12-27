from flask import Flask

app = Flask(__name__)
from requests_tor import RequestsTor

rt = RequestsTor(tor_ports=(9050,), tor_cport=9051)
@app.route("/")
def hello_world():
  rt.new_id()
  return rt.get("https://google.it").text
