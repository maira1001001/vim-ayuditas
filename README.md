# vim-ayuditas
algunas ayudas para usar vim 


vim

,jm -------  te lleva a models

,jc  -------- a controllers

,js -------- el buscador se pone dentro de spec/


search and replace

:%s/validate/valid/gc


--------------------------------------
PLUGINS: vi .vimrc.bundles


instalar gtk

vim --version, algunos no aparecen como clipboard

sudo apt-get install vim-gtk

vim .vimrc

agregas: set clipboard=unnamedplus

--------------------------------------------------------

instalar vim-vinegar

Plugin 'vim-vinegar'

:BundleInstall

-----------------------------------

indentar de arriba al final

gg=G

---------------------------------

tabs

abrir tab nuevo: selecciono archivo y le doy "ctrl + t"
      
desplazarse a la derecha : gt  (go tab)

ir al tab 3: 3 gt

-------------------------------------
plugin surround

cs ' " -> cambiar comillas simples por dobles

cs ( [ -> cambiar paréntesis por corchetes

-------------------------------
COPIAR

te posicionas entre 2 mismos elementos: enter "...", entre (...), entre [...]

yi '  -> yunk inside ' -> copia todo lo que esta dentro de las comillas

yi ( -> yunk inside ( -> copia todo lo que está dentro de los paréntesis

BORRAR

d /patron  -> detele hasta el patron, borra desde ppio de linea hasta "patron"

dt .   -> delete till "." , borrar hasta el punto

---------------------------------------
moverse entre archivos y saltos de líneas

PARA ATRÁS

ctrl + o -> vuelve al archivo anterior abierto, o a la última linea

PARA ADELANTE

ctrl + Y 

-----------------------------------

delete multiples lineas contiguas

d8+ -> borra desde el lugar, 8 lineas de arriba habia abajo

d7-  -> borra desde el lugar, 97lineas de abajo hacia arriba

--------------------------------------
delete bloques, cuerpos de metodos

dam -> delete arround method

dim  -> delete inner method

dt" -> delete till " (no borra las comillas)

df" -> delete force " (borras hasta las comillas inclusive)

D -> delete to end of line 

-----------------------------------------

plugin emmet 

-----------------------

change surrond /arround

ysiw" : Settings -> "Settings": 

------------------------------

SILVER SEARCH 

abrir con tab con vim todos los archivo "_form.html.erb" del directorio app   ->  vim -p $(ag -g "_form.html" app)

reemplanza "change_delay" por "delay_charge" sin abrir el vim, en todos los archivos que estén en la carpeta confirm -> ag -l "charge_delay" config | xargs sed -i "s/charge_delay/delay_charge/g"
