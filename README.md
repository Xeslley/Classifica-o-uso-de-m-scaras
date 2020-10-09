# Classifica-o-uso-de-mascaras
Projeto de TCC da pós-graduação na FIA, que teve como objetivo a criação de um modelo de classificação para identificar rostos e classificar se a pessoa esta utilizando a mascara de proteção corretamente.<br>
O Projeto é dividido em duas etapas:<br> 
1. Detectar rostos em uma imagem
2. Classificar os rostos encontrados

# Usar repositório com git

* Primeiro configure teus dados:<br>
  <code>git config --global user.name "Wesley Souza"</code><br>
  <code>git config --global user.email "wesleypatricksouza@gmail.com"</code><br>

* Clone o repositório:<br>
  <code>git clone https://github.com/Xeslley/Classifica-o-uso-de-mascaras.git</code>

* Crie um alias para o repositório para não precisar do link toda hora:<br>
  <code>git remote add origin git@github.com:Xeslley/Classifica-o-uso-de-mascaras.git</code>

* Apos fazer as mudanças, verificar com:<br>
  <code>git status</code>

* Adicionar mudanças com:<br>
  * Tudo junto<br>
      <code>git add .</code>
  * Por arquivo<br>
      <code>git add NOME_DO_ARQUIVO</code>

* Commitar no repositorio local ja com comentarario:<br>
  <code>git commit -m"Add comentario do commit"</code>

* Conferir se foi feito o commit com:<br>
  <code>git log</code>

* Subir a mudança no git hub com:<br>
  <code>git push</code>
 
# Configurar ambiente
### Com o anaconda instalado digitar os comandos abaixo
<code>conda create -n py3_6_tensorflow2_1 python=3.6 anaconda</code><br>
y<br>
<code>conda activate py3_6_tensorflow2_1</code><br>
<code>conda install scikit-learn</code><br>
<code>conda install pillow</code><br>
<code>conda install matplotlib</code><br>
<code>conda install pandas</code><br>
<code>conda install -c anaconda spyder</code><br>
y<br>
<code>conda install -c anaconda cudatoolkit</code><br>
y<br>
<code>conda install -c anaconda cudnn</code><br>
y<br>
<code>pip install tensorflow-gpu==2.1.0</code><br>
<code>pip install gast==0.2.2 -U</code><br>
<code>pip install tensorboard==2.0.0 -U</code><br>
<code>pip install tensorflow-estimator==2.0.0 -U</code><br>
<code>pip install opencv-contrib-python</code><br>
<code>pip install opencv-python</code><br>
<code>pip install cmake</code><br>
<code>pip install dlib --verbose</code><br>
<code>pip install face_recognition</code><br>
<code>pip install scikit-image</code><br>
#### Esta parte serve apenas para que o jupyter notebook mostre os tempos de execução
<code>pip install jupyter_contrib_nbextensions</code><br>
<code>jupyter contrib nbextension install --user</code><br>
<code>jupyter nbextension enable execute_time/ExecuteTime</code>

# Bases de dados
1. [Face Mask Detection](https://www.kaggle.com/andrewmvd/face-mask-detection)
2. [Base criada com imagens do google](https://github.com/Xeslley/Classifica-o-uso-de-mascaras/tree/main/Base_criado_com_fotos_google)
3. [Labeled Faces in the Wild](http://vis-www.cs.umass.edu/lfw/)

# Etapa 1 - Detectar rostos em imagens
* Copie as bases para a máquina local<br>
* Use o arquivo [TCC_exploratório+preprocessing.ipynb](https://github.com/Xeslley/Classifica-o-uso-de-mascaras/blob/main/TCC_explorat%C3%B3rio%2Bpreprocessing.ipynb) para tratar e preprocessar as informações (**lembre de editar os paths no arquivo de acordo com tua maquina local**)
* ***Atenção*** Na parte em que o script extrai uma amostra aleatória da base 3 para balancear as classes, não é feita a *annotation* e esta tarefa é por conta própria.<br>
<p> Uma opção é o LabelImg, mas pode ser feito por algum script que deixe com o padrão PASCAL VOC XML</p> [LabelImg](https://github.com/tzutalin/labelImg) [PASCAL VOC XML](http://host.robots.ox.ac.uk/pascal/VOC/)

* Use os arquivos [TCC_modelos_pretreinados_face_recognition_CNN.ipynb](https://github.com/Xeslley/Classifica-o-uso-de-mascaras/blob/main/TCC_modelos_pretreinados_face_recognition_CNN.ipynb), [TCC_modelos_pretreinados_HOG.ipynb](https://github.com/Xeslley/Classifica-o-uso-de-mascaras/blob/main/TCC_modelos_pretreinados_HOG.ipynb) e [TCC_modelos_pretreinados_Cascade.ipynb](https://github.com/Xeslley/Classifica-o-uso-de-mascaras/blob/main/TCC_modelos_pretreinados_Cascade.ipynb) para detectar as faces nas imagens (**lembre de editar os paths no arquivo de acordo com tua maquina local**).

# Etapa 2 - Classificar os rostos
Para esta etapa os dados já devem estar prontos por conta [TCC_exploratório+preprocessing.ipynb](https://github.com/Xeslley/Classifica-o-uso-de-mascaras/blob/main/TCC_explorat%C3%B3rio%2Bpreprocessing.ipynb).
#### Esta etapa demora bastante!!!
* Execute o notebook [TCC_clasificacao_imagens_baselines.ipynb](https://github.com/Xeslley/Classifica-o-uso-de-mascaras/blob/main/TCC_clasificacao_imagens_baselines.ipynb) para treinar diversos modelos de classificação do [scikit-learn](https://scikit-learn.org/stable/supervised_learning.html#supervised-learning) (**lembre de editar os paths no arquivo de acordo com tua maquina local**).<br>
* ***As etapas de transfer learning não obtiveram bom resultado para esta base :(*** <br>
* Após a etapa acima, tente criar um modelo agrupando alguns resultados dos classificadores treinados com o notebook [TCC_VotingClassifier.ipynb](https://github.com/Xeslley/Classifica-o-uso-de-mascaras/blob/main/TCC_VotingClassifier.ipynb) 
