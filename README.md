# Configurar TERMINAL - WINDOWS 11
# Guía paso a paso para personalizar PowerShell con temas, íconos y fuente personalizada.

## 1. Descargar "PowerShell" de la Microsoft Store

![Paso 1](Terminal-window/powershell-microsoft.png)


## 2. Establecer "PowerShell" como predeterminado:

### 2.1. Ingresando a Settings
![Paso 2.1](Terminal-window/powershell-settings.png)


### 2.2. Cambiando terminar por defecto
![Paso 2.2](Terminal-window/powersshell-settings-cambiar-terminal.png)

## 3. Instalar "Oh my Posh"

### 3.1. Ingresar al siguiente link:
https://ohmyposh.dev/docs/installation/windows

### 3.2. Copiamos el siguiente codigo:
![Paso 3](Terminal-window/oh-my-posh-instalar.png)

```powershell
winget install JanDeDobbeleer.OhMyPosh -s winget
```

## 4. Crear un perfil

### 4.1. Ingresar al siguiente link:
https://ohmyposh.dev/docs/installation/prompt

### 4.2. Copiamos el siguiente codigo:

![Paso 4](Terminal-window/crear-perfil.png)

```powershell
New-Item -Path $PROFILE -Type File -Force
```

## 5. Instalar "Hack Nerd Font"

### 5.1. Ingresar al siguiente link:
https://ohmyposh.dev/docs/installation/fonts
![Paso 5](Terminal-window/font.png)
### 5.1. Ingresar al siguiente link:
https://www.nerdfonts.com/
![Paso 5](Terminal-window/font-2.png)
### 5.1. Ingresar al siguiente link (ingresar a este link y busca el font):
https://www.nerdfonts.com/font-downloads

### 5.2. Descargar esta fuente, descomprimir e instalar todo:
![Paso 5](Terminal-window/font-hack-nerd-font.png)


## 6. Establecer "Hack Nerd Font" para el PowerShell como predeterminado

### 6.1. Primero ingresa a SETTINGS de la terminal de POWERSHELL -> Open JSON file (selecciona vscode si está)

![Paso 6](Terminal-window/open-JSON-file-terminal.png)

### 6.2. Configurar en vscode

![Paso 6](Terminal-window/6.establecer-hack-nerd-font.png)

```markdown
        "defaults": 
        {
            "colorScheme": "One Half Dark",
            "fontSize": 14,
            "fontFace": "Hack Nerd Font"
        },
```

## 7. Instalar el Tema en el archivo "$PROFILE"

### 7.1. Ingresar al siguiente link:
https://ohmyposh.dev/docs/installation/prompt

### 7.2. Ahora ejecuta este comando en tu terminal:
![Paso 7](Terminal-window/perfil-1.png)

```powershell
notepad $PROFILE
```

### 7.3. Tendremos esto y dejarlo ahí, que posteriormente agregaremos algo:
![Paso 7](Terminal-window/perfil-2.png)


### 7.4. Ingresar al siguiente link:
https://ohmyposh.dev/docs/installation/customize

![Paso 7](Terminal-window/perfil-3.png)

### 7.5. Ingresar al siguiente link:Ahora agregaremos esto al $PERFILE:
```markdown
oh-my-posh init pwsh --config ~/jandedobbeleer.omp.json | Invoke-Expression
```

### 7.6. Tendremos esto y dejarlo ahí, que posteriormente agregaremos algo:
![Paso 7](Terminal-window/perfil-4.png)


### 7.7. Ahora selecionaremos el tema (simplemente copias el nombre y lo pegas):
jandedobbeleer.omp.json -> agnoster.omp.json
![Paso 7](Terminal-window/perfil-5.png)

```markdown
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH/agnoster.omp.json" | Invoke-Expression
```

### 7.8. Pegamos en nuestro $PERFILE:
![Paso 7](Terminal-window/perfil-6.png)


## 8. Instalar los ICONOS (Personalización de archivos)

### 8.1. Ingresar al siguiente link:
https://github.com/devblackops/Terminal-Icons

### 8.2. Instalamos el siguiente modulo:
![Paso 8](Terminal-window/iconos.png)

```powershell
Install-Module -Name Terminal-Icons -Repository PSGallery
```


### 8.3. Importamos el siguiente codigo para los iconos:
![Paso 8](Terminal-window/iconos-2.png)

```markdown
Import-Module -Name Terminal-Icons
```

### 8.4. Pegamos en $PERFILE:
![Paso 8](Terminal-window/iconos-3.png)


## 9. Configurar en VSCODE

### 9.1. Ingresamos a VSCODE y Presionamos CTRL + P
```markdown
> Preferences: Open User Settings
```
![Paso 9](Terminal-window/vscode-1.png)

### 9.2. Agregamos la fuente:

```markdown
"terminal.integrated.fontFamily": "Hack Nerd Font"
```
![Paso 9](Terminal-window/vscode-2.png)


## 10. Autocompletado

Ingrese al tu terminal y presiona F2 para activar o desactivar autocompletado.




