# Entities
- Location, movement, physical properties to be wrapped in PhysicsBody
- Split Enemy into subclasses
- Externalise behaviour

# Factories
- Convert to non-static
- Instantiate object via reflection - use a binding dictionary <Enum.EnemyType, Class.Enemy>

# Renderer
- Models should pass a rendering strategy instead of the Renderer typechecking each model

# UI
- Actual ScreenElement and Button objects
- Event-based system

# World
- Find a way to eliminate typechecking when handling collisions (collision-response flags in model?)
- Entity interactions should be event-based (e.g. register damage zone when attacking, instead of directly searching for targets; the handler notifies all characters in the area and they decide how to react
- Custom collection for Entities and Tiles

# Events
- Damage should be event-based
- Entity removal should be event-based

# Input
- Command pattern
- Events

# Loop
- Extract Update and Render behaviour for different states
- Change state based on events (from menu buttons, level-change trigger, etc.)
