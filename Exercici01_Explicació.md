
## 1. Entidad Juego
```mermaid
flowchart TD
A[JUEGO] ---|1| B{Tiene} --- |1| C[Historia principal]
A --- |1|D{Tiene} ---|1|E[Personaje principal]
```

## 2. Superclase Historia principal
```mermaid
flowchart TD
A[Historia principal] ---|T,S| B((Misiones principales))
A ---|T,S| C(((Misiones secundarias)))
```

## 3. Relación entidad Historia Principal -- NPC's & MOBS
```mermaid
flowchart TD
A[Historia principal] ---|N| B{Tiene}
B --- |1|C[MOBS]
B --- |1|D[NPC's]
```
 
## 4. Superclase Mobs
 ```mermaid
flowchart TD
A[MOBS] --o |T,S|B((Tipo))
A --- C((Nivel))
A --- D((Daño))
```
## 5. Superclase NPC's
```mermaid
flowchart TD
A[NPC's] --o |T,S|B((Tipo))
A --o C((Dialogo))
```
## 6. Relación entidad Personaje principal -- Objetos
```mermaid
flowchart TD
A[Personaje principal] --- B{Tiene}
B --- C[Objeto]
```
## 7. Superclase objetos 
```mermaid
flowchart TD

```
## 8. Relación Personaje principal - Habilidad
 ```mermaid
flowchart TD

```
## 9. Subclase habilidades
```mermaid
flowchart TD

```
