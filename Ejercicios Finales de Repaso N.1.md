# SOLUCIÓN – Ejercicios Finales de Repaso

---

## 1. ¿Por qué es necesario que las computadoras representen los datos en binario?

Las computadoras usan el sistema **binario** porque internamente están compuestas por circuitos electrónicos que tienen dos únicos estados posibles: **encendido/apagado** o **alta/baja tensión**, los cuales se representan como **1 y 0** respectivamente.

Estos dos estados permiten que el procesamiento y almacenamiento de datos sea **más eficiente, confiable y económico**. Gracias a esto, cualquier tipo de información (como números, texto, imágenes o sonidos) puede codificarse en una secuencia de bits y ser entendida por la máquina.

---

## 2. Convierte el número binario `10011011` a decimal y a hexadecimal

### a) Binario a Decimal:

Para convertir de binario a decimal, multiplicamos cada bit por la potencia de 2 correspondiente:

```
10011011 = 1×2⁷ + 0×2⁶ + 0×2⁵ + 1×2⁴ + 1×2³ + 0×2² + 1×2¹ + 1×2⁰
         = 128 + 0 + 0 + 16 + 8 + 0 + 2 + 1
         = 155
```

**Resultado en decimal: 155**

### b) Binario a Hexadecimal:

Agrupamos los bits de 4 en 4 desde la derecha:

```
1001 1011 → 9 B
```

**Resultado en hexadecimal: 9B**

---

## 3. ¿Cómo se representa una imagen en formato PNG en el disco?

El formato **PNG (Portable Network Graphics)** es un tipo de archivo de imagen **sin pérdida**, que conserva la calidad original al comprimir la información.

En el disco, un archivo PNG se organiza en **bloques llamados "chunks"**. Los más importantes son:

- **Cabecera (`IHDR`)**: contiene información como el ancho, alto, tipo de color y profundidad de bits.
- **Datos de imagen (`IDAT`)**: almacenan los píxeles comprimidos usando el algoritmo **DEFLATE**.
- **Final de archivo (`IEND`)**: indica que no hay más datos.
- **Otros bloques opcionales**: como `tEXt` (metadatos), `PLTE` (paletas de colores), entre otros.

Cada imagen se representa en filas de píxeles y puede tener varios canales (como rojo, verde, azul y alfa para transparencia). El formato PNG es ideal cuando se necesita **preservar los detalles y la nitidez** de la imagen.

---

## 4. ¿Qué sucede si intentas almacenar un número mayor al que puede representar un byte (por ejemplo, 300)? ¿Cómo lo maneja Python?

Un **byte** solo puede almacenar valores entre **0 y 255**, ya que tiene **8 bits** (2⁸ = 256 posibles valores).

### a) En lenguajes como C:
Si se intenta almacenar un número mayor (como 300), ocurre un **desbordamiento**. Por ejemplo:

```
300 - 256 = 44
```

El valor almacenado sería incorrecto (44).

### b) En Python:

Los enteros (`int`) de Python **no tienen un límite fijo**, así que puedes trabajar con números grandes sin problema.

Sin embargo, si usas estructuras que simulan bytes, como `bytes` o `bytearray`, **sí hay restricciones**:

```python
bytes([300])
# Resultado: ValueError: bytes must be in range(0, 256)
```

Para representar 300 correctamente en **más de un byte**, puedes usar el método `to_bytes`:

```python
n = 300
b = n.to_bytes(2, byteorder='big')
print(b)  # Resultado: b'\x01,'
```

Aquí, `300` se guarda usando **2 bytes**, donde:
- `\x01` representa 256
- `\x2C` representa 44
- En conjunto: (256×1) + 44 = **300**

---
