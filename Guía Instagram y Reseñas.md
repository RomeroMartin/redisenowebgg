# Green Garden: conectar Instagram y reseñas de Google a la web nueva

Tiempo estimado: 15 a 20 minutos en total. No hace falta saber programar.

---

## Parte 1: Feed de Instagram (lo hace quien maneja las redes)

Vamos a usar **Behold** (behold.so), un servicio gratuito que toma las últimas publicaciones de @greengardenlaplata y se las pasa a la web. Cuando publiquen algo nuevo, aparece solo en la web.

### Antes de empezar

- Tener a mano el usuario y la contraseña de Instagram de **@greengardenlaplata**.
- La cuenta tiene que ser **profesional** (Empresa o Creador). Para revisarlo, entrá a Instagram, andá a **Perfil → ☰ Menú → Configuración → Tipo de cuenta y herramientas**. Si dice "Cambiar a cuenta personal", ya es profesional. Si dice "Cambiar a cuenta profesional", tocalo, elegí **Empresa** y categoría **Restaurante**. No se pierde nada.

### Paso a paso

1. Desde una computadora, entrá a **https://behold.so**.
2. Tocá **Sign up** (Registrarse) y creá una cuenta con un mail del restaurante. Conviene no usar un mail personal, para que la cuenta no dependa de una sola persona.
3. Confirmá el mail que te llega.
4. Dentro de Behold, tocá **Add source** o **Connect Instagram**.
5. Se abre Instagram. Iniciá sesión con **@greengardenlaplata** y tocá **Permitir** en todo lo que pida. Behold solo lee las publicaciones: no publica ni ve mensajes.
6. De vuelta en Behold, tocá **New feed** (Nuevo feed) y elegí la fuente de Instagram que acabás de conectar.
7. Cuando pregunte el tipo de feed, elegí **JSON**. No elijas "Widget": el formato JSON le da al diseñador las fotos sin diseño, para mostrarlas con el estilo de la web.
8. En la configuración del feed:
   - **Number of posts:** 9
   - **Include:** solo Fotos y Carruseles. Destildá Reels y videos si la opción existe.
9. Guardá. Vas a ver una dirección parecida a esta:
   `https://feeds.behold.so/XXXXXXXXXXXX`

### Qué me tienen que pasar

- ✅ **Esa dirección (URL del feed JSON).** Es lo único que necesito.
- Opcional: el mail con el que crearon la cuenta de Behold, para saber dónde está.

### Para tener en cuenta

- Si alguna vez cambian la contraseña de Instagram, puede que haya que volver a Behold y tocar **Reconnect**. Sin eso, el feed deja de actualizarse, pero la web sigue funcionando.
- El plan gratuito alcanza para una sola cuenta de Instagram, que es lo que necesitamos.

---

## Parte 2: Reseñas de Google (lo podés hacer vos mismo)

Esto no requiere la contraseña de Google del negocio: el servicio busca el restaurante en Google Maps y lee las reseñas públicas.

### ¿Se pueden mostrar solo las de 5 estrellas y que se renueven solas?

**Sí.** Los servicios de reseñas permiten filtrar por estrellas y se actualizan automáticamente: cuando alguien deja una reseña nueva de 5 estrellas, entra en la web y reemplaza a una más vieja.

Dos recomendaciones, para que no parezca maquillado:
- Mostrar igual el **puntaje promedio real** (por ejemplo "4,6 ★ en Google, 850 reseñas") con un enlace a **"Ver todas en Google"**. Da confianza, y además Google pide que no se presenten las reseñas como si fueran todas.
- Mostrar solo reseñas **con texto**. Las de 5 estrellas sin comentario no aportan.

### Paso a paso (con Trustindex, tiene plan gratuito)

1. Entrá a **https://www.trustindex.io** y tocá **Get started free** o **Crear widget gratis**.
2. Registrate con un mail del restaurante.
3. Cuando pregunte la plataforma, elegí **Google**.
4. En el buscador escribí **Green Garden La Plata** y seleccioná el restaurante correcto. Revisá que la dirección coincida.
5. Esperá a que cargue las reseñas (puede tardar unos minutos).
6. Elegí cualquier diseño de widget, por ejemplo "Slider" o "Grid". Da igual cuál, porque el diseño lo adapto yo a la web.
7. Buscá la sección de **filtros** (Filter / Filtro) y configurá:
   - **Calificación mínima: 5 estrellas**
   - **Ocultar reseñas sin texto:** sí
   - **Idioma:** todos, o solo español
   - **Orden:** más recientes primero
8. Guardá y tocá **Get code** o **Obtener código**. Vas a ver un bloque de texto que empieza con `<script` o `<div`.

**Si el plan gratuito no deja filtrar por 5 estrellas:** la alternativa es **Elfsight** (elfsight.com → "Google Reviews" widget). Se hace igual y tiene filtro por calificación, aunque su plan gratuito limita las visitas por mes. Avisame y vemos cuál conviene.

### Qué me tenés que pasar

- ✅ **El código del widget.** Copialo entero, tal cual aparece.
- ✅ El **puntaje promedio** y la **cantidad de reseñas** que figuran hoy en Google (los confirmo contra el widget).
- Opcional: el mail de la cuenta de Trustindex.

---

## Resumen: qué me llega

| De quién | Qué |
|---|---|
| Redes | URL del feed de Behold (`https://feeds.behold.so/...`) |
| Vos | Código del widget de reseñas + puntaje y cantidad actuales |

Con eso lo conecto a la web y queda funcionando solo.
