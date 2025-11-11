Adventurers of Venturia

A small, fantasy-themed dataset created for learning and practice. It contains 100 adventurers with randomized names, races, classes, kingdoms, levels, and gold amounts — perfect for experimenting with SQL and Python (pandas).

I made this dataset to practice working with smaller numbers, first designing the table in SQL and then filling it in and exploring it with Python (pandas). It’s perfect for experimenting with basic data analysis, SQL queries, and Python data manipulation.

Dataset Overview
Column	Type	Description
id	integer	Unique identifier for each adventurer
name	text	First name
last_name	text	Last name
race	text	Adventurer race (Human, Elf, Orc, Dwarf)
class	text	Adventurer class (Fighter, Mage, etc.)
kingdom	text	Kingdom the adventurer belongs to
level	integer	Character level
gold	integer	Amount of gold the adventurer owns


SQL Table Creation

CREATE TABLE Adventurers (
    id INTEGER PRIMARY KEY,
    name TEXT,
    last_name TEXT,
    race TEXT,
    class TEXT,
    kingdom TEXT,
    level INTEGER,
    gold INTEGER
);

Python: Names and Attributes
import random

names = ['Aster', 'Antara', 'Boldak', 'Balta', 'Corpik', 'Carnda', 'Defham', 'Dinsa', 'Enemaliz', 'Enderna', ... ]
last_names = ['Ashford', 'Blackwood', 'Coldmoor', 'Duskbane', 'Eboncrest', 'Frosthelm', ... ]
races = ['Human', 'Elf', 'Orc', 'Dwarf']
classes = ['Fighter', 'Ranger', 'Thief', 'Assassin', 'Mage', 'Bard', 'Merchant']
kingdoms = ['Ironhold', 'Silverwood', 'Bloodfang', 'Stormwind', 'Shadowmere', 'Frostveil', 'Duskmoor', 'Emberfall']

SQL Command Generator

for i in range(1, 101):
    name = random.choice(names)
    last_name = random.choice(last_names)
    race = random.choice(races)
    _class = random.choice(classes)
    kingdom = random.choice(kingdoms)
    level = random.randint(1, 100)
    gold = random.randint(0, 10000)

   print(f"INSERT INTO Adventurers (id, name, last_name, race, class, kingdom, level, gold) "
          f"VALUES ({i}, '{name}', '{last_name}', '{race}', '{_class}', '{kingdom}', {level}, {gold});")
