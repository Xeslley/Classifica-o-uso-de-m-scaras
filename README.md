# Classifica-o-uso-de-mascaras
Projeto de TCC da pós-graduação FIA, o objetivo é criar um modelo de classificação para identificar rostos e classificar se a pessoa esta utilizando a mascara de proteção corretamente.<br>
o Projeto é dividido em duas etapas:<br> 
1. detectar rostos em uma imagem
2. Classificar os rostos encontrados

# Usar repositório com git

* primeiro configure teus dados:<br>
  <code>git config --global user.name "Wesley Souza"</code><br>
  <code>git config --global user.email "wesleypatricksouza@gmail.com"</code><br>

* clone o repositório:<br>
  <code>git clone https://github.com/Xeslley/Classifica-o-uso-de-mascaras.git</code>

* crie um alias para o repositório para não precisar do link toda hora:<br>
  <code>git remote add origin git@github.com:Xeslley/Classifica-o-uso-de-mascaras.git</code>

* apos fazer as mudanças, verificar com:<br>
  <code>git status</code>

* adicionar mudanças com:<br>
  * tudo junto<br>
      <code>git add .</code>
  * por arquivo<br>
      <code>git add NOME_DO_ARQUIVO</code>

* commitar no repositorio local ja com comentarario:<br>
  <code>git commit -m"Add comentario do commit"</code>

* conferir se foi feito o commit com:<br>
  <code>git log</code>

* subir a mudança no git hub com:<br>
  <code>git push</code>
 
# configurar ambiente
### com o anaconda instalado digitar os comandos abaixo
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
2. [Base criada com imagens do goole]
3. [Labeled Faces in the Wild](http://vis-www.cs.umass.edu/lfw/)
