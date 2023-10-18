from sympy import symbols, integrate, Function, oo

# Definición de las variables y funciones
t, u = symbols('t u')
g1 = Function('g_1')(t)
g2 = Function('g_2')(t)
phi1 = Function('phi_1')(u)
phi2 = Function('phi_2')(u)

# Expresión para la integral
expr = (phi1.subs(u, g1) - phi2.subs(u, g2)) * (g1 - g2)

# Resolución de la integral
result = integrate(expr, (t, -oo, oo))

print(result)

