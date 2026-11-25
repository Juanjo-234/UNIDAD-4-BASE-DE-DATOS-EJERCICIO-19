# UNIDAD-4-BASE-DE-DATOS-EJERCICIO-19
1. Gestión de Usuarios y Perfiles (Herencia/Especialización)
usuario

Almacena la información central y general de todas las personas registradas en la plataforma.

Atributos: id_usuario (clave primaria), nombre, apellido, correo, rol y datos_cobro.

creador

Subtipo de usuario enfocado en los creadores de proyectos.

Atributos: id_usuario (clave primaria y foránea hacia usuario) junto con su nombre y apellido.

inversor

Subtipo de usuario enfocado en los patrocinadores o financiadores de los proyectos.

Atributos: id_usuario (clave primaria y foránea hacia usuario) y nivel_riesgo.

2. Gestión de Proyectos y Recompensas
proyecto

Contiene los detalles de las campañas de inversión publicadas en la plataforma.

Atributos: codigo_proyecto (clave primaria), titulo, categoria, descripcion, objetivo_financiero, estado, fecha_inicio, fecha_fin y id_usuario_creador (clave foránea hacia el creador).

recompensa

Administra los incentivos o retribuciones ofrecidas a cambio de los aportes financieros en los proyectos.

Atributos: id_recompensa (clave primaria), titulo, descripcion, valor_minimo, cantidad_maxima y codigo_proyecto (clave foránea).

3. Transacciones Financieras y Aportes
aporte

Registra las contribuciones económicas realizadas por los inversores a las diferentes campañas y recompensas.

Atributos: id_aporte (clave primaria), fecha, hora, id_usuario_inversor, id_recompensa y codigo_proyecto (claves foráneas que vinculan al inversor, la recompensa seleccionada y el proyecto financiado).

IMAGEN DE EJEMPLO DE UNA CONSULTA:
<img width="1097" height="331" alt="image" src="https://github.com/user-attachments/assets/7aab5117-b0b0-4116-b68f-55116526a510" />


4. Restricciones e Integridad Referencial
El script configura las reglas de validación mediante claves primarias y foráneas que garantizan la consistencia relacional del sistema, conectando correctamente los aportes con sus respectivos inversores, proyectos y recompensas, así como estructurando la jerarquía de usuarios y la autoría de los proyectos.
