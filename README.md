# AI-Server
AI Server run local


    sudo apt update && sudo apt upgrade -y

    sudo apt install python3 python3-pip

    python3 --version
    pip3 --version

    sudo apt install python3-venv

    python3 -m venv ai_env
    source ai_env/bin/activate

    pip install tensorflow

    pip install torch torchvision torchaudio

    pip install scikit-learn

    pip install jupyterlab

    sudo apt install nvidia-driver-550

    import tensorflow as tf
    print(tf.config.list_physical_devices('GPU'))

    pip install flask

create file app.py

    from flask import Flask, request, jsonify
    import tensorflow as tf

    app = Flask(__name__)

    @app.route('/predict', methods=['POST'])
    def predict():
        data = request.json
        # Add your AI model inference code here
        return jsonify({"prediction": "example_output"})

    if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)

    run the server 

    python app.py

Install docker

    sudo apt install docker.io
    sudo systemctl start docker
    sudo systemctl enable docker

    docker --version

Set Up Database

    sudo apt install postgresql postgresql-contrib

    sudo -u postgres createdb ai_database

Install Additional Tools

    sudo -u postgres createdb ai_database
    sudo snap install code --classic

Secure your Web

    sudo ufw allow ssh
    sudo ufw allow 5000
    sudo ufw enable

AUTOMATIC WITH sCRIPTS

    #!/bin/bash
    sudo apt update
    sudo apt install python3 python3-pip python3-venv
    python3 -m venv ai_env
    source ai_env/bin/activate
    pip install tensorflow flask
