Integrative activity evidence 1

Resumen
-------
Proyecto en Unity para la actividad integradora de Sistemas Multi‑Agente (MAS).
La idea es simular agentes que se mueven en un grid, evitan obstáculos y buscan objetivos.
El código está en C# y se usó un proyecto 3D básico de Unity.

Versión y editor
----------------
- Unity 2021.3 LTS (3D). Con otras versiones cercanas también debería abrir.
- TextMesh Pro aparece porque el paquete trae ejemplos, pero no es crítico para la lógica.

Contenido del paquete
---------------------
- Escena principal:
  - Assets/Scenes/SampleScene.unity
- Scripts (carpeta Assets/Scripts/):
  - SharedWorldState.cs
  - RobotBrain.cs
  - GridNav.cs
  - Metrics.cs
  - Chest.cs
  - obstaclescan.cs
  - Spawner.cs
  - Jewel.cs
  - Victories.cs
- Prefabs (Assets/Scripts/Prefabs/):
  - Capsule.prefab
  - Obstaculopared.prefab
  - Obstaculopared Variant.prefab
  - diamante_azul.prefab
  - diamante_rojo.prefab
  - diamante_verde.prefab
  - robot_azul.prefab
  - robot_rojo.prefab
  - robot_verde.prefab
- Materiales:
  - Assets/Materials/Blue.mat
  - Assets/Materials/Red.mat
- También vienen muchos ejemplos de TextMesh Pro (no son necesarios para la entrega)

Cómo abrir y ejecutar
---------------------
1) Abrir Unity Hub → Open → seleccionar o crear un proyecto 3D vacío.
2) Importar el paquete: Assets → Import Package → Custom Package… → seleccionar MAS_integrateact.unitypackage.
3) Abrir la escena Assets/Scenes/SampleScene.unity
4) Revisar en el Inspector:
   - Spawner: que tenga asignados los prefabs (robots/diamantes)
   - GridNav: tamaño del grid y límites.
   - Metrics/Victories: condiciones de conteo y fin
5) Dar Play

Comportamiento esperado
-----------------------
- Se instancian agentes (robots) y objetivos (diamantes).
- Los agentes se mueven en el grid y detectan obstáculos tipo pared.
- Se registran métricas básicas y se valida alguna condición de victoria.

Parámetros
- Spawner: cantidad de instancias y prefabs a usar.
- GridNav: dimensiones del grid y reglas de movimiento.
- Metrics/Victories: criterios de evaluación (p. ej., objetivos alcanzados o tiempo máximo).

Estructura del proyecto

```
└── Assets
    ├── Materials
    │   ├── Blue.mat
    │   ├── Green.mat
    │   └── Red.mat
    ├── Scenes
    │   └── SampleScene.unity
    └── Scripts
        ├── Chest.cs
        ├── GridNav.cs
        ├── Jewel.cs
        ├── Metrics.cs
        ├── New Shared World State.asset
        ├── Prefabs
        │   ├── Capsule.prefab
        │   ├── Obstaculopared Variant.prefab
        │   ├── Obstaculopared.prefab
        │   ├── diamante_azul.prefab
        │   ├── diamante_rojo.prefab
        │   ├── diamante_verde.prefab
        │   ├── robot_azul.prefab
        │   ├── robot_rojo.prefab
        │   └── robot_verde.prefab
        ├── RobotBrain.cs
        ├── SharedWorldState.cs
        ├── Spawner.cs
        ├── Victories.cs
        └── obstaclescan.cs
…
```

Notas
-----
- Si renombramos archivos o movemos carpetas, hay que re‑asignar referencias en el Inspector.
- Si al dar Play no pasa nada, normalmente es por prefabs sin asignar o scripts deshabilitados.
- Si Unity pide importar TextMesh Pro, aceptar; los ejemplos se pueden ignorar sin problema.

Equipo
------
- César Morán Macías
- Ana Paola Jiménez Sedano
- Ariana Guadalupe Rosales Villalobos
- Demmí Elizabeth Zepeda Rubio
- Luisa Merlo García
