## convert_decart_to_cartesian
# Перевод полярных координат
### Простой код на Ruby для перевода полярных координат (радиус r и угол theta) в декартовы координаты (x, y):

``` ruby

def polar_to_cartesian(r, theta)
  x = r * Math.cos(theta)
  y = r * Math.sin(theta)
  return x, y
end

def cartesian_to_polar(x, y)
  r = Math.sqrt(x**2 + y**2)
  theta = Math.atan2(y, x)
  return r, theta
end
```

# Пример использования полярные в декартовы:
```ruby
r = 5
degrees = 30.96
radians = degrees * Math::PI / 180
# theta = Math::PI / 4 # 45 градусов в радианах
x, y = polar_to_cartesian(r, radians)

puts "Декартовы координаты: (#{x.round(2)}, #{y.round(2)})"
```
# Пример использования декартовы в полярные:
``` ruby
x = 4.29
y = 2.57
r, theta = cartesian_to_polar(x, y)
degree = theta * 180 / Math::PI
puts "Полярные координаты: (#{r.round(2)}, #{degree.round(2)})"
```
