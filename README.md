# Crypzy: Cifrado Post-Cuántico Seguro  

Crypzy es una herramienta de cifrado avanzada diseñada para proporcionar **seguridad extrema** frente a ataques clásicos y cuánticos. Utiliza **AES-256 en modo CBC**, junto con **PBKDF2 + SHA3-512** y un esquema de autenticación **HMAC-SHA3-512**, asegurando la máxima resistencia ante computadoras convencionales y cuánticas.

---

## Características del cifrado 

✔️ **Cifrado simétrico robusto:** Usa **AES-256 CBC** con IV aleatorio.  
✔️ **Derivación de claves segura:** PBKDF2 con **200,000 iteraciones y SHA3-512**.  
✔️ **Protección contra manipulación:** HMAC-SHA3-512 garantiza la integridad del mensaje.  
✔️ **Formato seguro:** Los datos cifrados se almacnan en JSON con Salt, IV, Ciphertext y HMAC.  
✔️ **Resistencia cuántica:** Aumenta el costo computacional para ataques cuánticos.  
✔️ **Código optimizado:** Seguro, eficiente y fácil de implementar.  

---

## 🔐 Esquema de Cifrado  

- Se genera un **Salt** y un **IV** aleatorio.  
- Se deriva una clave de **512 bits** con **PBKDF2-SHA3** (200,000 iteraciones).  
- La clave se divide en **AES-256 Key** y **HMAC Key**.  
- Se cifra el mensaje con **AES-256-CBC**.  
- Se genera un **HMAC-SHA3-512** sobre los datos cifrados.  
- El resultdo se almacena en **JSON**, incluyendo salt, IV, ciphertext y HMAC.


Ejemplo de salida JSON cifrada:
```json
{
  "salt": "15b63aa57028ce326414529e2b286a56",
  "iv": "0bfc93284e20f4f02d27bdec8efc498a",
  "ciphertext": "MriqQiSy5FnYvhZE9l9KSQ==",
  "hmac": "f4a2880e574b86095e16faa88b1ffda9fa910b1af545f88b6f66821e85524b55a66e08ba034f2803b076f75855c1de8f47b3624022661d4f17ac3141ec413e98"
}
```


**DEV a base de DroidScript JS By OXSR**
