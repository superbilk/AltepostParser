# AltePostParser
Ruby parser for altepost.sipgate.net - Get all dishes, by date

```ruby
altepost = AltepostParser.new         # uses current week (29/2015 e.g.)
puts altepost.dishes_of_today         # today is 17.07.2015

# { :meal_id=>"meal152",
#   :food_type=>"fisch",
#   :name=>"Meeresfrüchtegratin mit Reis",
#   :date=>"17.07.2015",
#   :image_file=>#<Tempfile: (closed)>,
#   :image_url=>"http://altepost.sipgate.net/showPic.php?meal=152&pic=image.jpg"
# }
# { :meal_id=>"meal153",
# :food_type=>"vegi",
# :name=>"Gemüseauflauf",
# :date=>"17.07.2015",
# :image=>nil,
# :image_url=>nil
# }

# Compare with http://altepost.sipgate.net/?kw=29/2015


puts altepost.dishes_of_the_day('07.07.2015')

# { :meal_id=>"meal138",
#   :food_type=>"carne",
#   :name=>"Focaccia-Burger mit Lamm-Rinderhack",
#   :date=>"07.07.2015",
#   :image_file=>#<Tempfile: (closed)>,
#   :image_url=>"http://altepost.sipgate.net/showPic.php?meal=138&pic=image.jpg"
# }
# { :meal_id=>"meal139",
#   :food_type=>"vegi",
#   :name=>"Veggi-Burger",
#   :date=>"07.07.2015",
#   :image=>nil,
#   :image_url=>nil
# }

# Compare with http://altepost.sipgate.net/?kw=28/2015
```
