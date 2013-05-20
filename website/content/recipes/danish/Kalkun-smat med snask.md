title: Kalkun-smat med snask
type: recipe
category: recipes/danish
tags: [dinner]
image:
    url: http://i.imgur.com/alqzKg0.jpg
    where: right
---
*Tilføjet af Anders Lindbo*

recipe.py
---------
    ::Python
    import netto
    import kitchen

    # for 6 persons
    ingredients = {
        'kalkun': (1.0, 'kg'),
        'fløde': (0.25, 'l'),
        'bacon': (0.2, 'kg'),
        'dåsetomater': (1.0, 'ds'),
        'tomatpuré': (1.0, 'ds'),
        'cherrytomater': (1.0, 'bakke'),
        'peberfrugt' (1.0, 'stk'),
        'løg': (2.0, 'whatever'),
        'hvidløg': (1.0, 'whatever'),
        'ris': (1.0, 'kg')
    }

    def makeDinner(personCount=6, baconFactor=1):
        ingredientFactor = personCount/5.0
        ingredients['bacon'] = (ingredients['bacon'][0]*baconFactor,
                              ingredients['bacon'][1])
        shoppingList = [(name, ingredients[name][0]*ingredientFactor, ingredients[name][1]) 
                        for name in ingredients]
        groceries = netto.fetchIngredients(ingredients)
        
        # the following three steps should
        # be executed in parallel (feel free to import pycsp)
        kitchen.loadIngredients(groceries)
        kitchen.roastUntilDone('kalkun')
        kitchen.roastUntilCrisp('bacon')
        kitchen.chopFinely('peberfrugt', 'løg', 'cherrytomater', 'hvidløg')
        kitchen.slice('kalkun', thickness='1cm')
        kitchen.roastUntilGolden('løg', 'hvidløg')
        kitchen.addIngredients['dåsetomater', 'tomatpuré', 'fløde', 
                             'bacon', 'cherrytomater', 'peberfrugt']
        kitchen.spizeUp('paprika', 'chili', 'pebber')
        kitchen.boilSeperately['ris']
        return kitchen.getSmask()


    def makeDatalogDinner(personCount=4, baconFactor=1):
        return makeDinner(personCount*1.5, baconFactor**2)
