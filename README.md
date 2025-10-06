# Tarea03_SXE

# Práctica Docker con Alpine

En esta práctica se han realizado varias tareas utilizando la imagen de Alpine. Se registran los comandos usados y una breve explicación de cada paso.

---

## 1. Descargar la imagen "alpine" sin arrancarla

   ```bash
   docker pull alpine
   ```
<img width="737" height="159" alt="Captura desde 2025-10-06 11-48-34" src="https://github.com/user-attachments/assets/36d3ec54-c8d1-40e1-90ca-5091ec9a658a" />

---

## 2.Crear un contenedor sin ponerle nombre

   ```bash
   docker create alpin
   ```
<img width="590" height="48" alt="Captura desde 2025-10-06 12-05-21" src="https://github.com/user-attachments/assets/f717c8c5-7862-4458-9363-aa416be33e9a" />

---
Para obtener el nombre:
   ```bash
   docker ps -a
   ```
<img width="998" height="130" alt="Captura desde 2025-10-06 12-07-31" src="https://github.com/user-attachments/assets/cd877a3b-9ea6-4a28-a7fa-0e08a3e3eb55" />

## 3.Crear un contenedor con nombre dam_alp1

   ```bash
   docker run -it --name dam_alp1 alpine sh
   ```

## 4.Comprobar la IP y hacer ping a google.com
Obtener IP del contenedor y Hacer ping desde el contenedor:
   
 
    docker inspect -f '{{ .NetworkSettings.IPAddress }}' dam_alp1
    ping -c 4 google.com

<img width="997" height="262" alt="Captura desde 2025-10-06 12-17-40" src="https://github.com/user-attachments/assets/86ca063f-3038-48b5-b573-34a39bab9b90" />

## 5. Crear un contenedor dam_alp2 y probar comunicación entre contenedores
-Dentro de dam_alp2, hacer ping a dam_alp1 (usando la IP obtenida antes):
    
    
    docker run -it --name dam_alp2 alpine sh
    ping -c 4 <IP_de_dam_alp1>
    

    

    
   
  
