# Hummingbird_IA
Um projeto de aprendizagem do Unity Learn para uma IA de um beija-flor aprendendo a coletar nectar.

## Programas necessários:
  > Unity 2022.1.14f1 ou mais atual;
  
  > Anaconda3;
  
  #### Configurando um novo ambiente no Anaconda
  ```
    # Abra o console do anaconda e com o comando abaixo, crie um novo ambiente para usar o MLAgents:
    > conda create -n NOMEDOAMBIENTE(ml-agents-1.5) python=3.9
    
    # Para ativar o novo ambiente use:
    > conda activate NOMEDOAMBIENTE(o mesmo nome que usou para criar o ambiente)
    
    # Com o ambiente ativo vamos instalar o MLAgents:
    > pip install mlagents
  ```
  
  #### Instalação do Pytorch
  ```
    # Antes de instalar o pytorch caso você tenha uma placa de vídeo habilitada para utilizar CUDA.
    Então vamos configurar isso primeiro. Você pode verificar sua placa de vídeo no site da NVidia, em: https://developer.nvidia.com/cuda-gpus
    
    # Nesse artigo da MEDIUM, em: https://medium.com/data-hackers/como-instalar-nvidia-cuda-83aa21dde069, você encontra instruções mais detalhadas para a instalação do CUDA e cuDNN.
    
    # Após instalar o CUDA use esse comando para instalar o pytorch.
    > conda install pytorch torchvision torchaudio pytorch-cuda=11.7 -c pytorch -c nvidia
    
    # Caso não tenha uma placa de vídeo então vamos usar apenas o processador.
    > conda install pytorch torchvision torchaudio cpuonly -c pytorch
 ```
  
  #### Iniciando o treinamento do nosso agente
  ```
    # Para iniciar o treinamento basta digitar o comando:
    > mlagents-learn ./trainer_config.yaml --run-id hb_01
    
    # Onde ./trainer_config.yaml é nosso arquivo de configuração para nossa rede neural. Você pode checar mais informações e configurações no GitHub do MLAgents, em: https://github.com/Unity-Technologies/ml-agents/blob/main/docs/Training-Configuration-File.md.
    
    # hb_01 é o nome de identificação do seu treinamento
  ```
  
  #### Tensorboard
  ```
  Aqui podemos acompanhar a evolução do nosso agente via dashboard web. No prompt do anaconda, navegue até a pasta onde estão os arquivos do treinamento e digite:
  > tensorboard --logdir summaries
  ```
