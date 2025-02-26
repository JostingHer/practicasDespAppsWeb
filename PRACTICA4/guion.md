# **Práctica 2: Despliegue de Aplicaciones con Proxy Inverso**

## **1. Configuración del Entorno**

### **Máquina: Escritorio Pr. Combinada Serv. Ap.**
Se han instalado los siguientes componentes:
- PHP
  
  ![Instalamos PHP](./img/image.png)
- Nginx
- Node.js
- MySQL
- **Pendiente**: Complementos de PHP
- **Opcional**: phpMyAdmin
  
  ![Versiones de todas](./img/image-1.png)

---
## **2. Despliegue 1: Aplicación PHP en Apache (Puerto 8080)**

### **Configuración**
- Apache escucha en el puerto **8080**.
- URL de acceso: [http://localhost:8080](http://localhost:8080)
- Aplicación demo de sesiones anteriores.

#### **Pasos realizados:**
1. **Configuración del puerto en Apache**
   
   ![Configurando el puerto 8080](./img/image-2.png)

2. **Creación del VirtualHost para la app PHP**
   
   ![Creando un VirtualHost para la app PHP](./img/image-3.png)

3. **Habilitación del sitio en Apache**
   
   ![Habilitando el sitio](./img/image-4.png)

4. **Descarga de la aplicación desde GitHub**
   
   ![Descargando la app de GitHub](./img/image-5.png)

5. **Configuración de MySQL**
   
   ![MySQL](./img/image-6.png)

6. **Resultado final de la aplicación PHP**
   
   ![Resultado final](./img/image-8.png)

---
## **3. Despliegue 2: Aplicación Node.js (Puerto 3000)**

### **Configuración**
- Node.js ejecutando en el puerto **3000**.
- URL de acceso: [http://localhost:3000](http://localhost:3000)
- Aplicación demo de sesiones anteriores.

#### **Pasos realizados:**
1. **Importación de la base de datos** (archivo SQL sobre "deseos")
   
   ![Instalamos](./img/image-9.png)

2. **Ejecución de la aplicación Node.js**
   
   ```sh
   npm run start
   ```

3. **Resultado final de la aplicación Node.js**
   
   ![Resultado final](./img/image-10.png)

---
## **4. Configuración del Proxy Inverso con Nginx**

### **Configuración**
- **Sitio 1:** [http://php.local](http://php.local)
- **Sitio 2:** [http://node.local](http://node.local)
- **Puerto:** 80
- **Configuraciones adicionales:** Archivo `hosts` modificado.

#### **Pasos realizados:**
1. **Configuración del proxy inverso en Nginx**
   
   ![Configuración del proxy inverso](./img/image-11.png)

2. **Habilitación y reinicio de Nginx**
   
   ![Habilitar y reiniciar Nginx](./img/image-12.png)

3. **Modificación del archivo hosts** y reinicio
   
   ![Configurar el archivo hosts](./img/image-13.png)

4. **Verificación de `php.local`**
   
   ![PHP.local](./img/image-14.png)

5. **Verificación de `node.local` (con la app corriendo en el puerto 3000)**
   
   ![Node.local](./img/image-15.png)

---

### ✅ **Despliegue exitoso de ambas aplicaciones con proxy inverso configurado correctamente.** 🚀