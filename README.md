# Rails Decal Lecture 5

### Files Created/Modified

```
# Models
app/models/trainer.rb
app/models/pokemon.rb

# Migrations
db/migrate/20180309031505_create_pokemons.rb
db/migrate/20180309031518_create_trainers.rb
db/migrate/20180309031608_add_trainer_id_to_pokemons.rb

# Schema
db/schema.rb

```

### Rails Terminal Commands

```
rails generate model Pokemon name:string attack:integer
rails g model Trainer name:string age:integer

rails g migration AddTrainerIdToPokemons trainer_id:integer

rails db:migrate
```