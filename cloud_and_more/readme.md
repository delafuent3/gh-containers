# cloud-and-more-intro
Intro to Cloud

## Powershell
1. Lo primero que haremos sera instalar una linea de comandos. Windows ya tiene una linea de comandos instalada por defecto, pero vamos a instalar una mas actualizada. Y esta herramienta se llama Powershell \

Descarga Powershell
```
https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.4
```

Una vez que el archivo esta descargado, procedemos a la instalacion, solo hacemos doble click y seguimos el asistente. La instalacion sera con las opciones por defecto

Ese iconoen el boton instalar, nos dice que vamos a tener que dar permiso de administrador.

Una vez que el asistente ha terminado, hacemos click en finalizar.


2. Instalar usando winget
   Abrir powershell y ejecutar el siguiente comando
````
winget install --id Microsoft.PowerShell --source winget
````


## Windows Terminal


Para instalar Windows terminal, abrimos Microsoft Store y buscamos windows terminal, aqui vamos a instalar la que no dice preview.

Seleccionamos de la lista de resultados y despues hacemos click en Get. Esto va a instalar la aplicacion automaticamente, no nos pedira ninguna informacion o que demos click en algun boton

Una vez finalizada la instalacion, cerramos Microsoft store, damos click al boton inicio y podemos ver que en las recomendaciones, aparece Terminal recien instalado, damos click al icono para abrir la aplicacion.

Para ser honesto, la unica funcionalidad practica que tiene esta aplicacion, es que puedes abrir multiples tabs, lo que powershell no te permite, y lo que los usuarios de Mac y Linux siempre te echaran en cara. Gracias Microsoft, problema solucionado


### Install windows terminal using winget
````
winget install -e --id Microsoft.WindowsTerminal
````

## Oh-My-Posh

Instalacion en windows (Docs)
````
https://ohmyposh.dev/docs/installation/windows
````

1. Installar ohmyposh (Winget)
````
winget install JanDeDobbeleer.OhMyPosh -s winget
````
NOTE: Restart terminal after installation

2. Install Font
   Download NerdFont (JetBrains Mono) and install it

https://github.com/ryanoasis/nerd-fonts/releases/download/v3.2.1/JetBrainsMono.zip

2. Install Font
````
oh-my-posh font install JetBrainsMono 
````



Check for shell in use (Powershell by default)

````
oh-my-posh get shell 
````



3. Descargar archivo de configuracion

NOTE: My favorite PowerLevel10k
````
https://github.com/JanDeDobbeleer/oh-my-posh/blob/main/themes/powerlevel10k_classic.omp.json 
````



4. Modify/Crear powershell profile

Run

````
notepad $PROFILE 
````


Create Powershell profile

````
New-Item -Path $PROFILE -Type File -Force 
````
Una vez creado el perfil, lo modificamos. \
ejecutar
````
notepad $PROFILE 
````


Download OhMyPosh profile (to create a local profile and customize it as required)


````
https://ohmyposh.dev/docs/themes
````



Modify PowerShell Profile adding the path to the file.



oh-my-posh init pwsh --config '<PATH_TO_JSON_FILE>' | Invoke-Expression



oh-my-posh init pwsh --config 'https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/main/themes/jandedobbeleer.omp.json' | Invoke-Expression


For Remote file
````
oh-my-posh init pwsh --config '<PATH_TO_JSON_FILE>' | Invoke-Expression
````




For local file


Configuracion para archivo almacenado localmente
````
oh-my-posh init pwsh --config '<PATH>' | Invoke-Expression
````

5.

3. Update Windows Terminal configuration to select Nerd Font

Settings -> Defaults -> Appearance -> Text -> Font face

Seleccionar la fuente deseada, en este caso "JetBrainsMono Nerd Font"


4. Restart PowerShell

6. Restart PowerShell


````
& $PROFILE
````

Transcendent

Additional configurations, Transient prompt
````
      "type": "prompt"
    }
  ],
  "transient_prompt": {
    "background": "transparent",
    "foreground": "#ffffff",
    "template": "{{ .Shell }}> "
  },
  "version": 2
}
````

Additional configurations, New Line
````
      "type": "prompt"
    }
  ],
  "transient_prompt": {
    "background": "transparent",
    "foreground": "#ffffff",
    "template": "{{ .Shell }}> ",
    "newline": true
  },
  "version": 2
}
````

### MS Instructions
````
https://learn.microsoft.com/en-us/windows/terminal/tutorials/custom-prompt-setup
````


## 4. GIT


## 5. SSH Key

## WSL
Install WSL
````
wsl.exe --install
````
Restart after installation has finished


## Docker Desktop
1. Create account
2. Enable wsl feature
2. Download Installation file
```
https://docs.docker.com/desktop/setup/install/windows-install/
```

3. Install
4. OR install from Microsoft Store



## Github
Create Account

## GIT
1. Install using winget
````
winget install --id Git.Git -e --source winget
````

2. Create SSH key

3. Add public key to GitHub account
4. Set Git (UserName, User Email)


## WSL
NOTE, solve grayed out Nested VT, VirtualBox

```
https://learn.microsoft.com/en-us/answers/questions/2194528/i-cannot-enable-the-nested-vt-x-amd-v-to-both-vmwa?forum=windowsclient-all&referrer=answers
```


NOTE: Download VMWare tools 17
````
https://archive.org/details/vmware-tools-isos-player-17.0.0
````