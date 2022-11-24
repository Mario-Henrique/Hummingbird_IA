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
    # Antes de instalar o pytorch caso você tenha uma placa de vídeo habilitada para utilizar CUDA então vamos configurar isso primeiro. Você pode verificar sua placa de vídeo nesse site: https://developer.nvidia.com/cuda-gpus
    # Aqui você encontra instruções mais detalhadas na instalação do CUDA e cuDNN: https://medium.com/data-hackers/como-instalar-nvidia-cuda-83aa21dde069
    
    # Após instalar o CUDA use esse comando para instalar o pytorch. Lembre-se de mudar a versão do CUDA
    > conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
    
    # Caso não tenha uma placa de vídeo então vamos usar apenas o processador.
    > conda install pytorch torchvision torchaudio cpuonly -c pytorch
  ```
  
  #### Iniciando o treinamento do nosso agente
  ```
    # Para iniciar o treinamento basta digitar o comando:
    > mlagents-learn -h
  ```
