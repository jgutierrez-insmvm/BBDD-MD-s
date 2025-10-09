# Explicación Model Entitat/Relació
<img width="1384" height="703" alt="image" src="https://github.com/user-attachments/assets/02eba969-b057-4546-82f0-f2e6739ffa22" />

>[!NOTE]
>Explicaré cada entidad una por una con capturas
>

[Enlace al modelo](https://drive.google.com/file/d/1PMjvULH9lWNbXRQLLn1yJnrlc8chnM7f/view?usp=sharing)

## 1. Entidad Juego
<img width="60%" height="35%" alt="image" src="https://github.com/user-attachments/assets/777a7d62-e967-4e2e-bafa-2fa6d8c3949b" />

- La entidad **Juego** se relaciona con la entidad **historia principal**, la cual solo puede ser una relación 1:1
- Tambien se relaciona con la entidad **Personaje principal**, el cual solo puede ser una relación 1:1
- Obligatoriamente tienen que relacionarse entre ellas.

## 2. Superclase Historia principal
 <img width="60%" height="35%" alt="image" src="https://github.com/user-attachments/assets/04ff0220-0403-4302-8b4e-f356610cbbf5" />

- Esta es una **superclase**
- Hay dos tipos de misiones dentro de la historia, misiones principales y secundarias
- Son atributos que no tienen porque tener un valor, por defecto lo tienen, hasta que se completan y quedarian marcadas como `nulas`
- El atributo misiones secundarias pueden contener muchos valores, ya que dentro de la entidad `**Historia principal**` tienen que haber diversos atributos.
- Obligatoriamente la **superclase** tiene que relacionarse con las dos *subclases* (`T`) y tambient debe aparecer ambos atributos dentro de la entidad (`S`)

## 3. Relación entidad Historia Principal -- NPC's & MOBS
  <img width="60%" height="35%" alt="image" src="https://github.com/user-attachments/assets/e919b53d-3d93-43ab-9a52-1599d9b13939" />

- La historia debe tener obligatoriamente `NPC's` y `Mobs` ya que sin estos la historia pierde sentido.
- Una historia principal puede tener muchos `NPC's` y `Mobs`, mas no al revés, ambas entidades no pueden participar en mas de una historia principal.

## 4. Superclase Mobs
  <img width="60%" height="35%" alt="image" src="https://github.com/user-attachments/assets/ff2877c9-10aa-4e26-8bed-c8f2352bed0c" />
  
- El tipo de mob no puede ser nulo, ya que siempre debe marcarse como `vivo`, `muerto`, `nivel de agresividad`, etc...
- Debe ser **total y solapada** ya que no puede existir un mob sin `nivel`, ni `tipo`, ni `daño` nulo.

  ## 5. Superclase NPC's
  <img width="60%" height="35%" alt="image" src="https://github.com/user-attachments/assets/3468af83-20e5-45fb-bc75-b89155fcca92" />
  
- Ambos atributos deben ser **no nulos**, ya que todos los NPC's deben tener un `dialogo` y deben identificarse con un `tipo`
  - Mercadero
  - NPC de dialogo basico
  - NPC que entrega objetos
  - Etc...
>[!NOTE]
> Estos tipos no están definidos, solo es un ejemplo.

- Debe ser **total** y **solapada** ya que no puede existir un NPC sin dos de esas caracteristicas.
  
## 6. Relación entidad Personaje principal -- Objetos
<img width="60%" height="35%" alt="image" src="https://github.com/user-attachments/assets/c621c37e-0b18-4036-933c-215c00f3757e" />

- La entidad `personale principal` **puede tener varios objetos** pero el `objeto` **no puede pertenecer** a mas de un `personaje principal`.
- No es obligatorio que el `personaje principal` tenga `objetos`, puede pasarse la historia sin objetos.

## 7. Superclase objetos 
<img width="60%" height="35%" alt="image" src="https://github.com/user-attachments/assets/34df6ca8-1e92-46ab-8f49-666eadab4311" />

- El objeto **no tiene que pertenecer obligatoriamente** a todos los tipos de *subclase*, por eso es parcial (`P`), al ser objetos unicos, **tampoco pueden ser dos tipos de subclase a la vez**, por eso es disjunta (`D`)

## 8. Relación Personaje principal - Habilidad
  <img width="120" height="308" alt="image" src="https://github.com/user-attachments/assets/3a18f1c2-f697-496d-9728-a9a7dbf05542" />

  - **Obligatoriamente** el personaje debe tener `habilidades`
  - El mismo personaje **puede tener todas las habilidades que quiera** pero las habilidades **no pueden tener mas de un dueño**
 
## 9. Subclase habilidades
<img width="373" height="198" alt="image" src="https://github.com/user-attachments/assets/aa27d881-c084-435c-9b44-70af44b3784f" />

  - Cada habilidad debe tener como minimo el `Cooldown` definido y debe ser identificada como habilidad `pasiva` o `activa`
