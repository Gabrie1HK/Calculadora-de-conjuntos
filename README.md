# Documentación del Código: Calculadora de Conjuntos

## Descripción General
La Calculadora de Conjuntos es una aplicación web interactiva que permite realizar operaciones matemáticas con conjuntos. Los usuarios pueden definir un conjunto universal y varios subconjuntos, y realizar operaciones como unión, intersección, diferencia y diferencia simétrica. Los resultados se muestran tanto en formato de extensión como de comprensión.

## Estructura del Código
El código está dividido en tres secciones principales:

1. **HTML**: Define la estructura de la página, incluyendo los campos de entrada, botones y secciones de resultados.
2. **CSS**: Proporciona el diseño visual de la aplicación, incluyendo estilos para botones, modales y mensajes de error.
3. **JavaScript**: Contiene la lógica para validar los conjuntos, realizar operaciones y mostrar resultados.

## Funcionalidades Principales

### 1. Definición de Conjuntos
- Los usuarios pueden ingresar:
  - Un conjunto universal (U).
  - Hasta cuatro subconjuntos (A, B, C, D).
- Los conjuntos se ingresan como cadenas separadas por comas (ejemplo: `1,2,3`).

### 2. Validaciones
- **Conjunto Universal**:
  - No puede estar vacío.
  - Debe contener solo caracteres válidos (letras, números, comas y espacios).
- **Subconjuntos**:
  - Los elementos deben pertenecer al conjunto universal.
  - No se permiten caracteres especiales.
- **Operaciones**:
  - Los conjuntos seleccionados para operaciones no pueden estar vacíos.

### 3. Operaciones Disponibles
- **Operaciones Básicas**:
  - Unión (`A ∪ B`)
  - Intersección (`A ∩ B`)
  - Diferencia (`A - B`)
  - Diferencia Simétrica (`A △ B`)
- **Operaciones Múltiples**:
  - Unión de todos los conjuntos (`A ∪ B ∪ C ∪ D`)
  - Intersección de todos los conjuntos (`A ∩ B ∩ C ∩ D`)
  - Diferencia de todos los conjuntos (`A - B - C - D`)
  - Diferencia Simétrica de todos los conjuntos (`A △ B △ C △ D`)

### 4. Generación de Conjuntos Aleatorios
- Genera un conjunto universal aleatorio con entre 8 y 15 elementos.
- Genera subconjuntos aleatorios que pertenecen al conjunto universal.

### 5. Limpieza de Datos
- Limpia todos los campos de entrada y resultados.

### 6. Modal de Ayuda
- Proporciona una guía de uso para la calculadora.

## Estructura del Código JavaScript

### Variables Globales
```javascript
let conjuntos = {
    U: new Set(),
    A: new Set(),
    B: new Set(),
    C: new Set(),
    D: new Set()
};
```
Estas variables almacenan los conjuntos definidos por el usuario.

### Funciones Principales

#### 1. `parseSet(input)`
Convierte una cadena de texto en un conjunto eliminando duplicados y espacios.

#### 2. `validateSets()`
Valida los conjuntos ingresados por el usuario:
- Verifica que el conjunto universal no esté vacío.
- Asegura que los subconjuntos contengan solo elementos válidos y que pertenezcan al conjunto universal.

#### 3. `updateSets()`
Actualiza las variables globales con los valores ingresados por el usuario.

#### 4. Operaciones de Conjuntos
- **Unión**: `union(setA, setB)`
- **Intersección**: `intersection(setA, setB)`
- **Diferencia**: `difference(setA, setB)`
- **Diferencia Simétrica**: `symmetricDifference(setA, setB)`
- **Complemento**: `complement(setA, universal)`

#### 5. `displayResult(title, resultSet, operation)`
Muestra los resultados de una operación en la sección de resultados.

#### 6. `performOperation(operation, set1, set2)`
Realiza operaciones básicas entre dos conjuntos.

#### 7. `performBinaryOperation()`
Realiza operaciones binarias seleccionadas por el usuario.

#### 8. `generateRandomSets()`
Genera conjuntos aleatorios para pruebas rápidas.

#### 9. `clearAll()`
Limpia todos los campos de entrada y resultados.

#### 10. Validaciones Adicionales
- **Caracteres Especiales**: `hasInvalidCharacters(input)`
- **Conjuntos Vacíos en Operaciones**: `validateOperationSets(set1, set2)`

## Estilo Visual (CSS)
- **Diseño Responsivo**: Se adapta a pantallas pequeñas con media queries.
- **Botones**: Estilo moderno con degradados y efectos de hover.
- **Modal de Ayuda**: Fondo semitransparente con contenido centrado.

## Cómo Usar la Calculadora
1. Ingrese un conjunto universal y los subconjuntos deseados.
2. Seleccione una operación básica o múltiple.
3. Presione el botón correspondiente para calcular.
4. Revise los resultados en la sección de resultados.
5. Use el botón de ayuda (`?`) para obtener más información.

## Notas
- Los conjuntos deben definirse correctamente antes de realizar operaciones.
- Los resultados se muestran en formato de extensión y comprensión.
- Los mensajes de error guían al usuario en caso de entradas inválidas.

## Autor
Elaborado por Gabriel Espinoza. Puedes encontrar más proyectos en su [GitHub](https://github.com/Gabrie1HK).
