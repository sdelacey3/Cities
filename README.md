# Cities
list, dictionary, and tuple project

import pprint

## Dictionary: (Collaborative)
cities = {
'Abu Dhabi' :
{'Country': 'United Arab Emirates', 'Population (in millions)': 1.45, 'Fact': '"Abu Dhabi" means "Father of the Gazelle"'},
'London' :
{'Country' : 'England', 'Population (in millions)' : 8.982, 'Fact' : 'London was founded by the Romans in 50 AD'}, 
'Berlin':
{'Country' : 'Germany', 'Population (in millions)': 3.769, 'Fact': 'Berlin has the largest train station in Europe'}
}

# List: (Sydney)
visitedCities = ['Abu Dhabi','London','Berlin']

def printCityList(listOfCities):
  for i in range(len(listOfCities)-1):
    print(listOfCities[i] + ', ' , end = '')
  print('and ' + listOfCities[-1] + '.')

def newCities():
  print('You have visted ', end = '')
  printCityList(visitedCities)
  while True:
    print('Enter a new city you have visited: (blank to quit)')
    newCity = input()
    if newCity == '':
      break
    visitedCities.append(newCity)
  print('Your list of cities has been updated to: ' , end = '')
  printCityList(visitedCities)


## Tuple: (Jack)
stableCities = ('Berlin', 'Abu Dhabi')
def vivaLaRevolution (city):
  print ('Where shall we revolutionize?')
  if city not in cities.keys():
    print('Woah there Napoleon, we don\'t have that city on record and is off limits. Pal.')
  elif city not in stableCities:
    cities[city].setdefault('Revolutionized', 'You betcha')
    print ('Long live Liberty')
  else:
    print('Hey, what do you think you\'re doing to our glorious nation?')
  

pprint.pprint(cities['Abu Dhabi'])
pprint.pprint(cities['London'])
pprint.pprint(cities['Berlin'])
newCities()
vivaLaRevolution('Abu Dhabi')
vivaLaRevolution('London')
vivaLaRevolution('Sydney')
