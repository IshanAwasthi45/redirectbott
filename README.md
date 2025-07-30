# redirectbott
from flask import Flask, request

app = Flask(__name__)

@app.route('/')
def redirect_handler():
    code = request.args.get('code')
    return f"Authorization Code: {code}"

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=10000)

