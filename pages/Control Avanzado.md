---
cssClasses: cards ,cards-cols-4
---
#Control_Avanzado 
- [OneNote](https://upcomillas-my.sharepoint.com/:o:/r/personal/zamora_comillas_edu/_layouts/15/guestaccess.aspx?guestaccesstoken=w7P2mmBoYLomNQPRHAEA8KQYLBZcYl9Iu2UAppszEEk%3D&folderid=086888c26268c4a2eb48454bd45ded153)

# Books
```dataview
table
  WHERE type = "book"
  AND contains(file.tags, "#Control_Avanzado") AND
  !contains(file.name, ".Desktop") 
  ```
# Modelado

[Modelado de plantas](Modelado%20de%20plantas.md)
[[Diseño de controles por respuesta en frecuencia]]
```dataview
table  
  WHERE contains(file.tags, "#Control_Avanzado") AND contains(file.tags, "#modelado") AND
  !contains(file.name, ".Desktop") 
  ```
# Controles
[[Guia de elección de controles]]
```dataview
table  
  WHERE contains(file.tags, "#Control_Avanzado") AND contains(file.tags, "#control") AND
  !contains(file.name, ".Desktop") 
  ```
# All
```dataview
table  
  WHERE contains(file.tags, "#Control_Avanzado") AND
  !contains(file.name, ".Desktop") 
  ```

## Evaluacion
- Problemas -> simuladores
```run-python
practicas = 0
inter_lab = 0 
final_lab = 0
inter_teo = 0
final_teo = 0
nota = inter_lab*0.15+0.15*practicas+ 0.2* final_lab + inter_teo*0.10+ final_teo * 0.4
print (nota)
```

## Temas
- [[Introduccion al  control Avanzado]]
   [[Laboratorio de Control Avanzado]]

