# SUPERHERO
# Base class for Superhero
class Superhero:
    def __init__(self, name, superpower, weakness):
        self.name = name
        self.superpower = superpower
        self.weakness = weakness
    
    def display_hero_info(self):
        return f"{self.name} has the superpower of {self.superpower} and a weakness for {self.weakness}."

    def use_superpower(self):
        return f"{self.name} uses their superpower of {self.superpower} to save the day!"

# Subclass for a specific superhero
class FlyingHero(Superhero):
    def __init__(self, name, superpower, weakness, flight_speed):
        super().__init__(name, superpower, weakness)
        self.flight_speed = flight_speed
    
    # Polymorphism with an overridden method
    def use_superpower(self):
        return f"{self.name} flies at {self.flight_speed} km/h using their superpower of {self.superpower}!"

# Create instances of the superheroes
hero1 = Superhero("Mighty Max", "super strength", "kryptonite")
hero2 = FlyingHero("Sky Specter", "flight", "storms", 800)

# Display hero information and actions
print(hero1.display_hero_info())
print(hero1.use_superpower())

print(hero2.display_hero_info())
print(hero2.use_superpower())
