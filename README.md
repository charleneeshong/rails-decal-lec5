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

### Rails Console

If you'd like to play around with the app, clone it, `bundle install`, and `rails db:migrate`

Then, open `rails console` in terminal & try out these commands


```
p = Pokemon.create(name: 'Pikachu', attack: 5)
t = Trainer.create(name: 'Ash', age: 16)

p.trainer = t
p.save

t.pokemons.create(name: 'Squirtle', attack: 10)
t.pokemons.create(name: 'Bulbasaur', attack: 8)

t.pokemons

squirtle = Pokemon.find_by(name: 'Squirtle')
squirtle.trainer

```