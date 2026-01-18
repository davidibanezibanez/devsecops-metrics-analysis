# **Reporte 1: Algoritmo búsquedas intercontinentales en Google para literatura científica y literatura gris**  

Fecha: 04-08-2025

## **Objetivo**  
Realizar búsquedas en Google desde diferentes países de los 5 continentes, utilizando consultas relacionadas con investigaciones en ciencias de datos (ejemplo: `"security ci/cd"`), filtrando enlaces no deseados mediante expresiones regulares y exportando los resultados en un archivo CSV.  

Se utilizarán **3 VPN gratuitas** (Proton VPN, Windscribe y TunnelBear) para garantizar diversidad geográfica, y la extensión **Link Extractor** en Firefox para extraer enlaces.  

## **Selección de VPNs**  
Se eligieron las siguientes VPNs gratuitas bajo criterios de seguridad y disponibilidad geográfica:  

### **1. Proton VPN**  
- **Nivel de seguridad**: Alto (basada en Suiza, política de no registros).  
- **Flexibilidad geográfica**:  
  - No permite selección manual de países en versión gratuita.  
  - En nuestras pruebas, solo se conectó automáticamente a EE.UU. y Países Bajos.  
- **Limitaciones**: Ideal para Europa y Norteamérica, pero sin control sobre ubicación.  

### **2. Windscribe**  
- **Nivel de seguridad**: Medio-Alto (política de no registros, pero con menos auditorías que Proton).  
- **Flexibilidad geográfica**:  
  - Permite elegir algunos países de América del Norte, Europa y Asia.  
  - **No incluye** Oceanía, África ni Sudamérica en versión gratuita.  
- **Limitaciones**: Ofrece GBs limitados gratis.

### **3. TunnelBear**  
- **Nivel de seguridad**: Medio (auditorías independientes, pero con restricciones de datos).  
- **Flexibilidad geográfica**:  
  - Permite seleccionar manualmente países de **todos los continentes**, incluidos África y Oceanía.  
- **Limitaciones**:  
  - Ofrece GBs limitados gratis.  
  - Puede bloquearse tras alcanzar el límite.  

**Nota sobre otras VPNs**:  
Se descartaron opciones por falta de políticas claras de seguridad.  

## **Requisitos Previos**  
1. **Navegador**: Firefox (recomendado por compatibilidad con extensiones).  
2. **Extensiones**:  
   - **Link Extractor**.  
3. **VPNs**:  
   - Proton VPN 
   - Windscribe 
   - TunnelBear 

## **Paso a Paso**  

### **1. Instalación y Configuración de VPNs**  
#### **Proton VPN**  
1. Descargar e instalar desde su sitio oficial.  
2. Crear una cuenta gratuita.  
3. Conectar (no permite elegir país; se asignará automáticamente).  

#### **Windscribe**  
1. Instalar y registrarse.  
2. Seleccionar un país disponible. 
3. Conectar (no permite países bloqueados en versión gratuita).  

#### **TunnelBear**  
1. Instalar y crear cuenta.  
2. Elegir manualmente un país  
3. Conectar (vigilar el límite de datos).  

### **2. Configuración de Firefox y Link Extractor**  
1. **Instalar Link Extractor**:  
   - Buscar "Link Extractor" como extensión para Firefox en instalar.  

2. **Agregar Permisos de Host**:  
   - Buscar opción para permisos de Host en las opciones de la extensión. 

3. **Filtro Regex para Excluir Enlaces No Deseados**:  
   - Abrir la extensión Link Extractor.  
   - En "Filter Patterns", ingresar:  
     ```regex
     ^((?!google|youtube).)*$
     ```  
   - Esto excluirá enlaces de `google.com/support`, `youtube.com`, etc.  

### **3. Realización de Búsquedas**  
1. **Conectar VPN** 
2. **Buscar en Google**:  
   - Abrir Google.com (verificar en la parte inferior izquierda de la pantalla de Google que la ubicación sea la deseada).  
   - Ejecutar búsqueda (ejemplo: `"security ci/cd"`).  
3. **Extraer Enlaces**:  
   - Hacer clic derecho en la pantalla y click en el icono de Link Extractor.  
   - Aplicar el filtro regex preconfigurado.  
   - Exportar resultados como CSV 

### **4. Repetir el Proceso por Continente**  
Para cubrir los 5 continentes, se recomienda:  

#### **Norteamérica**  
- **VPN recomendada**: Proton VPN (Estados Unidos).   

#### **Sudamérica**  
- **VPN recomendada**: TunnelBear (Brasil). 

#### **Europa**  
- **VPN recomendada**: Proton VPN (Países Bajos).  

#### **Asia**  
- **VPN recomendada**: Windscribe (China (Hong Kong)).  

#### **África**  
- **VPN recomendada**: TunnelBear (Sudáfrica).  

#### **Oceanía**  
- **VPN recomendada**: TunnelBear (Nueva Zelanda).    

## **Consideraciones Finales**  
- **Limitaciones de VPNs gratuitas**:  
  - Proton VPN no permite selección manual de países.  
  - Windscribe excluye regiones clave.  
  - TunnelBear tiene un ancho de banda muy limitado.  
