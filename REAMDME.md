console.log("Startup Nation, le retour");

console.log("les prénom et les nom des entrepreneurs sont ;");
let name = entrepreneurs.map((names) => names.first + " " + names.last);
console.log(name);  

console.log(
  "Remplace la date de naissance par l'âge de l'entrepreneur qu'il aurait aujourd'hui"
);
let now = entrepreneurs.map(
  (nows) =>
    nows.first + " " + nows.last + " aurait " + (2021 - nows.year) + " ans"
);
console.log(now);

console.log("Remplace-les clés");
var replace_key = entrepreneurs.map(
  ({ first: firstName, last: lastName, ...rest }) => ({
    firstName,
    lastName,
    ...rest,
  })
);
console.log(replace_key);

console.log(
  "Filtre dans cette liste les entrepreneurs qui sont nés dans les années 70 ;"
);
let result = replace_key.filter(
  (element) => element.year > 1969 && element.year < 1980
);
console.log(result);