# vim-ayuditas
algunas ayudas para usar vim 


## vim

###Buscador ,t

1. te lleva a models  `,jm`

2. te lleva a controllers  `,jc` 

3. te lleva a spec   `,js`

### Search and Replace

1. Busca y reemplaza *validate* por *valid* desde el inicio(`g`) pidiendo confirmacion (`c`)

`:%s/validate/valid/gc`

-------------------------------------------------------------------------------

### PLUGINS: 

> ubicación: vi .vimrc.bundles

#### Instalar GTK

> Para copiar del clipboar

1. `sudo apt-get install vim-gtk`

vim --version, algunos no aparecen como clipboard

2. Abrir el archivo de configuración 

`vim .vimrc`

3. Agregas

`set clipboard=unnamedplus`

#### Instalar vim-vinegar

1. Agregar `Plugin 'vim-vinegar'`

2. ejecutar `:BundleInstall`

#### Indentar

1. indentar de arriba al final  `gg=G`

#### Tabs

1. abrir tab nuevo: selecciono archivo y le doy `ctrl + t`
2. desplazarse a la derecha : `gt`  (go tab)
3. ir al tab 3: `3 gt`

#### plugin surround

 1. cambiar comillas simples por dobles: `cs ' "`  (cs: change surround)
 2. cambiar paréntesis por corchetes: `cs ( [`

#### Copiar

> te posicionas entre 2 mismos elementos: enter "...", entre (...), entre [...]

1. copia todo lo que esta dentro de las comillas: `yi '`  (yank inside `'` )
2. copia todo lo que está dentro de los paréntesis: `yi (` (yank inside `(` ) 

#### Borrar

1.   -> detele hasta el patron, borra desde ppio de linea hasta "patron"

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

## SILVER SEARCH

> abrir con tab con vim todos los archivo "_form.html.erb" del directorio app  
> `vim -p $(ag -g "_form.html" app)`


> reemplanza "change_delay" por "delay_charge" sin abrir el vim, en todos los archivos que estén en la carpeta confirm
> `ag -l "charge_delay" config | xargs sed -i "s/charge_delay/delay_charge/g"`
