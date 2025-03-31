https://clemenssiebler.com/posts/deploying-deepseek-r1-azure-machine-learning/

>az account set --subscription xxxx

>az login --tenant "xxxx"

>az configure --defaults workspace=workspace-centralus group=rg_centralus

>az ml environment create -f environment.yaml

then rebuild the image until seeing the container registry, use the container registry URL in endpoint.yaml.

>az ml online-endpoint create -f endpoint.yaml

>az ml online-deployment create -f deployment.yaml --all-traffic

then run the RAG_DeepSeep.ipynb
