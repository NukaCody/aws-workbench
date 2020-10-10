FROM amazonlinux:2

RUN amazon-linux-extras install -y ansible2 golang1.11 python3.8 docker postgresql10 \
    && curl -sL https://rpm.nodesource.com/setup_lts.x | bash - \
    && yum install -y jq nodejs tar git unzip \
    && python3.8 -m pip install --upgrade pip \
    && python3.8 -m pip install aws-lambda-powertools aws-sam-cli aws-shell boto3 c7n cloudformation-cli cloudformation-cli-go-plugin cloudformation-cli-python-plugin \
    && python3.8 -m pip install awswrangler httpie ipykernel numpy pandas rdk sagemaker scikit-learn \
    && python3.8 -m pip install autopep8 black yapf bandit flake8 mypy pycodestyle pydocstyle pylint \
    && npm install -g aws-cdk @aws-amplify/cli \
    && curl -Lo /usr/local/bin/copilot https://github.com/aws/copilot-cli/releases/download/v0.4.0/copilot-linux-v0.4.0 \
    && chmod +x /usr/local/bin/copilot \
    && curl -Lo /tmp/hugo.tar.gz https://github.com/gohugoio/hugo/releases/download/v0.76.3/hugo_0.76.3_Linux-64bit.tar.gz \
    && tar -xvf /tmp/hugo.tar.gz --directory /tmp/ \
    && mv /tmp/hugo /usr/local/bin/hugo \
    && chmod +x /usr/local/bin/hugo \
    && curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && ./aws/install
