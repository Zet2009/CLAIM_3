# Rubineta – Pretenzijų registravimo sistema (prototipas)

Šis projektas yra **veikiantis prototipas** pretenzijų registravimo sistemai, sukurtai pagal dokumentą „Pretenzijų registravimo sistema – 2025.docx“.

## 🚀 Kaip naudoti?

1. Atsisiųskite visus failus
2. Atidarykite `index.html` naršyklėje
3. Nenaudoja serverio – viskas veikia per `file://` ir `localStorage`

## 🔐 Prisijungimas

- **Administratorius**: prisijunkite ir pakeiskite vartotojo rolę į `admin` per naršyklės konsolę:
```js
let users = JSON.parse(localStorage.getItem('users'));
if (users && users.length > 0) {
    users[0].role = 'admin';
    localStorage.setItem('users', JSON.stringify(users));
}