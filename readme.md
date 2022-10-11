


    1) `npm install package-name -o` → Instalar una dependencia opcional
    2) Se pueden generar conflictos cuando se tienen paquetes que usan la misma dependencia pero en versiones diferentes. Para evitar esto se puede simular una instalación con `npm install package-name —dry-run`. Con esto se simula la instalación pero sin agregar ningún paquete, de manera que se verifique si se puede realizar de manera segura una instalación de dicho paquete; si no hay ningún conflicto se procede a instalar de la manera convencional.
    3) `npm install package-name@0.15.0` → Instalar la versión especifica de un paquete. Si luego se quiere instalar la versión más reciente se usa `npm install package-name@latest`.
    4) `npm install` → Instala las dependencias que estén dentro de un package.json.
    5) `npm list`
