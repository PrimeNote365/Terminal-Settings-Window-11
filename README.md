![image](https://github.com/user-attachments/assets/bf893514-20c8-42c5-93cd-ba52104a13b6)![image](https://github.com/user-attachments/assets/f0114595-2d1e-49c4-bb94-8f1d7015e077)![image](https://github.com/user-attachments/assets/64028fb0-c1fb-4d1e-a9fc-143383213de2)![image](https://github.com/user-attachments/assets/cee0ba9d-f78f-4a8f-a335-ce871d51296f)![image](https://github.com/user-attachments/assets/4316cb8b-9ed3-4cc8-b280-2d5f6c50dba8)![image](https://github.com/user-attachments/assets/6b0fa046-ed4f-4cad-841c-5db49ddfa5c1)![image](https://github.com/user-attachments/assets/a55fc0e7-7a5e-491e-baab-83987b931e99)![image](https://github.com/user-attachments/assets/2859b0a4-80d6-4e5d-a9e9-7eeb910c5d51)![image](https://github.com/user-attachments/assets/5f2ff262-188b-44dd-a920-ac8f09890770)![image](https://github.com/user-attachments/assets/350c38ac-0958-4256-9202-c214539fda19)![image](https://github.com/user-attachments/assets/1ccb7818-f298-4c3c-94ea-5d80fcd3b4b9)![image](https://github.com/user-attachments/assets/d17d40de-4040-4c37-968c-8bead3e2bd60)![image](https://github.com/user-attachments/assets/11248950-9ae9-4d95-93b5-99d38566512c)# Terminal-settings Windows


## 1. Descargar "PowerShell" de la Microsoft Store

![Paso 1](Terminal-window/powershell - microsoft.png)


## 2. Establecer "PowerShell" como predeterminado:

### 2.1. Ingresando a Settings
![Paso 2.1](Terminal-window/powershell - settings.png)


### 2.2. Cambiando terminar por defecto
![Paso 2.2](Terminal-window/powersshell - settings - cambiar terminal.png)

## 3. Instalar "Oh my Posh"

Ingresar al siguiente link:
https://ohmyposh.dev/docs/installation/windows

![Paso 3](Terminal-window/oh my posh - instalart.png)

```powershell
winget install JanDeDobbeleer.OhMyPosh -s winget
```

## 4. Crear un perfil

Ingresar al siguiente link:
https://ohmyposh.dev/docs/installation/prompt

![Paso 4](Terminal-window/crear perfil.png)

```powershell
New-Item -Path $PROFILE -Type File -Force
```

## 5. Instalar "Hack Nerd Font"

Ingresar al siguiente link:
https://ohmyposh.dev/docs/installation/fonts
Ingresar al siguiente link:
https://www.nerdfonts.com/
Ingresar al siguiente link (ingresar a este link y busca el font):
https://www.nerdfonts.com/font-downloads

![Paso 5](Terminal-window/font.png)

![Paso 5](Terminal-window/font 2.png)

### 5.1. Descargar esta fuente, descomprimir e instalar todo:

![Paso 5](Terminal-window/font hack nerd font.png)


## 6. Establecer "Hack Nerd Font" para el PowerShell como predeterminado

### 6.1. Primero ingresa a SETTINGS de la terminal de POWERSHELL -> Open JSON file (selecciona vscode si está)

![Paso 6](Terminal-window/font hack nerd font.png)

### 6.2. Configurar en vscode

![Paso 6](Terminal-window/6. establecer hack nerd font.png)

```markdown
        "defaults": 
        {
            "colorScheme": "One Half Dark",
            "fontSize": 14,
            "fontFace": "Hack Nerd Font"
        },
```

## 7. Instalar el Tema en el archivo "$PROFILE"

Ingresar al siguiente link:
https://ohmyposh.dev/docs/installation/prompt

![Paso 7](Terminal-window/perfil 1.png)

Ahora ejecuta este comando en tu terminal:
```powershell
notepad $PROFILE
```

Tendremos esto y dejarlo ahí, que posteriormente agregaremos algo:
![Paso 7](Terminal-window/perfil 2.png)


Ingresar al siguiente link:
https://ohmyposh.dev/docs/installation/customize

![Paso 7](Terminal-window/perfil 3.png)

Ahora agregaremos esto al $PERFILE:
```markdown
oh-my-posh init pwsh --config ~/jandedobbeleer.omp.json | Invoke-Expression
```

Tendremos esto y dejarlo ahí, que posteriormente agregaremos algo:
![Paso 7](Terminal-window/perfil 4.png)


Ahora selecionaremos el tema (simplemente copias el nombre y lo pegas):
jandedobbeleer.omp.json -> agnoster.omp.json
![Paso 7](Terminal-window/perfil 5.png)

```markdown
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH/agnoster.omp.json" | Invoke-Expression
```

Pegamos en nuestro $PERFILE:
![Paso 7](Terminal-window/perfil 6.png)


## 8. Instalar los ICONOS (Personalización de archivos)

Ingresar al siguiente link:
https://github.com/devblackops/Terminal-Icons

Instalamos el siguiente modulo:
![Paso 8](Terminal-window/iconos.png)

```powershell
Install-Module -Name Terminal-Icons -Repository PSGallery
```


Instalamos el siguiente modulo:
![Paso 8](Terminal-window/iconos 2.png)

Copiamos lo siguiente y pegamos en $PERFILE:
```markdown
Import-Module -Name Terminal-Icons
```

Pegamos:
![Paso 8](Terminal-window/iconos 3.png)


## 9. Configurar en VSCODE

Presionamos CTRL + P

ingresamos a:
```markdown
> Preferences: Open User Settings
```
![Paso 9](Terminal-window/vscode 1.png)

Agregamos la fuente:


```markdown
"terminal.integrated.fontFamily": "Hack Nerd Font"
```
![Paso 9](Terminal-window/vscode 2.png)


## 10. Autocompletado

Ingresa a tu terminal POWERSHELL y presiona F2 para activar y desactivar la lista de comandos que usaste antes.




