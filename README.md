# vim-ayuditas
algunas ayudas para usar vim 

## vim

### Buscador ,t

1. te lleva a models  `,jm`
2. te lleva a controllers  `,jc` 
3. te lleva a spec   `,js`

### Search and Replace

1. Busca y reemplaza *validate* por *valid* desde el inicio(`g`) pidiendo confirmacion (`c`) `:%s/validate/valid/gc`

### PLUGINS: 

ubicación: vi .vimrc.bundles

#### Instalar GTK

Para copiar del clipboar. vim --version, algunos no aparecen como clipboard

1. `sudo apt-get install vim-gtk`
2. Abrir el archivo de configuración: `vim .vimrc`
3. Agregas `set clipboard=unnamedplus`

#### Instalar vim-vinegar

1. Agregar `Plugin 'vim-vinegar'`
2. ejecutar `:BundleInstall`

#### Indentar

1. indentar de arriba al final:  `gg=G`

#### Tabs

1. abrir tab nuevo: selecciono archivo y le doy `ctrl + t`
2. desplazarse a la derecha : `gt`  (go tab)
3. ir al tab 3: `3 gt`

#### plugin surround

 1. cambiar comillas simples por dobles: `cs ' "`  (cs: change surround)
 2. cambiar paréntesis por corchetes: `cs ( [`

#### Copiar

te posicionas entre 2 mismos elementos: enter "...", entre (...), entre [...]

1. copia todo lo que esta dentro de las comillas: `yi '`  (yank inside `'` )
2. copia todo lo que está dentro de los paréntesis: `yi (` (yank inside `(` ) 

#### Borrar

1. detele hasta el patron, borra desde principio de linea hasta "patron": `d/patron`
2. delete till `.` , borrar hasta el punto: `dt .` 

#### Moverse entre archivos y saltos de líneas

PARA ATRÁS

vuelve al archivo anterior abierto, o a la última linea
> ctrl + o 

PARA ADELANTE

> ctrl + Y 

#### Delete 

* multiples lineas contiguas

1. Borra desde el lugar, 8 lineas de arriba habia abajo: `d8+`
2. Borra desde el lugar, 7 lineas de abajo hacia arriba: `d7-`

* bloques, cuerpos de metodos

1. delete arround method: `dam`
2. delete inner method: `dim`
3. delete till " (no borra las comillas): `dt"`
4. delete force " (borras hasta las comillas inclusive): `df"`
5. delete to end of line : `D`

#### plugin emmet 

1. yank surrond /arround: `ysiw"` : Settings -> "Settings": 
(yank surround inner word: agarra la palabra y le pone comiilas al rededor)


## SILVER SEARCH

1. abrir con tab con vim todos los archivo "_form.html.erb" del directorio app : `vim -p $(ag -g "_form.html" app)`
2. reemplanza **change_delay** por **delay_charge** sin abrir el vim, en todos los archivos que estén en la carpeta confirm: `ag -l "charge_delay" config | xargs sed -i "s/charge_delay/delay_charge/g"`
