# Liste des Expressions Régulières en PHP

| Expression Régulière | Description |
| --- | --- |
| `/^\d+$/` | Correspond à une chaîne de caractères contenant uniquement des chiffres. |
| `/^[a-zA-Z]+$/` | Correspond à une chaîne de caractères contenant uniquement des lettres (majuscule ou minuscule). |
| `/^[a-z0-9_]+$/i` | Correspond à une chaîne de caractères contenant uniquement des lettres, chiffres et underscores (insensible à la casse). |
| `/^[\w-]+$/` | Correspond à une chaîne de caractères contenant uniquement des lettres, chiffres, underscores et tirets. |
| `/^[\d]{3}-[\d]{2}-[\d]{4}$/` | Correspond à un numéro de sécurité sociale américain (format XXX-XX-XXXX). |
| `/^(\d{4})-(\d{2})-(\d{2})$/` | Correspond à une date au format YYYY-MM-DD. |
| `/^[A-Z][a-z]+\s[A-Z][a-z]+$/` | Correspond à un nom complet au format "Prénom Nom" avec des lettres majuscules initiales. |
| `/^\S+@\S+\.\S+$/` | Correspond à une adresse email simple (ne vérifie pas la validité complète). |
| `/^(https?:\/\/)?([a-z0-9\-\.]+)\.([a-z]{2,6})(\/[\w\.-]*)*\/?$/i` | Correspond à une URL de base (http ou https, avec un domaine et un chemin optionnel). |
| `/^(\+?\d{1,4}[\s-])?(?!0+\s,?\d)([2-9]\d{2}[\s-]?\d{3}[\s-]?\d{4})(\s?(x\|ext)\d{1,5})?$/` | Correspond à un numéro de téléphone international avec extension optionnelle. |
| `/^[01]?[0-9]\|2[0-3]:[0-5][0-9]$/` | Correspond à un format d'heure valide (HH:MM, 24 heures). |
| `/^[0-9a-fA-F]{32}$/` | Correspond à un hash MD5 (32 caractères hexadécimaux). |
| `/^[A-Z0-9]{8}-[A-Z0-9]{4}-[A-Z0-9]{4}-[A-Z0-9]{4}-[A-Z0-9]{12}$/i` | Correspond à un UUID (Universally Unique Identifier) de version 4. |
| `/^([A-Z][a-z]+)(\s[A-Z][a-z]+)*$/` | Correspond à un nom propre (par exemple, "John Doe"). |
| `/^[A-Za-z]+(\s[A-Za-z]+)*$/` | Correspond à une phrase contenant uniquement des lettres et des espaces. |
| `/^[\d]{5}(-[\d]{4})?$/` | Correspond à un code postal américain (format XXXXX ou XXXXX-XXXX). |
| `/^\d{1,2}\/\d{1,2}\/\d{4}$/` | Correspond à une date au format DD/MM/YYYY. |
| `/^(?:[1-9]\|[12][0-9]\|3[01])\/(?:0[1-9]\|1[0-2])\/\d{4}$/` | Correspond à une date valide au format DD/MM/YYYY (vérifie les jours et mois valides). |
| `/^[\p{L}]+(?:[\s\p{L}]+)*$/u` | Correspond à une chaîne de texte avec des lettres Unicode (prend en compte les caractères spéciaux). |
| `/^\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2}$/` | Correspond à une date et une heure au format YYYY-MM-DD HH:MM:SS. |
| `/^\d+(\.\d{1,2})?$/` | Correspond à un nombre décimal avec jusqu'à deux décimales. |
| `/^\d+(?:,\d{3})*(?:\.\d+)?$/` | Correspond à un nombre avec séparateurs de milliers (par exemple, "1,234,567.89"). |
| `/^\d{1,3}(?:\.\d{1,3}){3}$/` | Correspond à une adresse IP au format IPv4. |
| `/^(?:[0-9A-Fa-f]{1,4}:){7}[0-9A-Fa-f]{1,4}$/` | Correspond à une adresse IP au format IPv6 (non-compressée). |
| `/^(?:0x)?[0-9A-Fa-f]+$/` | Correspond à une chaîne hexadécimale (avec ou sans préfixe "0x"). |
| `/^(?=.*[A-Za-z])(?=.*\d)[A-Za-z\d]{8,}$/` | Correspond à un mot de passe contenant au moins une lettre, un chiffre, et ayant au moins 8 caractères. |
| `/^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$/` | Correspond à un mot de passe complexe avec lettres majuscules, minuscules, chiffres, et caractères spéciaux (au moins 8 caractères). |
| `/^\d{1,2}\/\ d{1,2}/\d{2}$/` | Correspond à une date au format DD/MM/YY (sur deux chiffres). |
| `/^([a-z0-9]+[-_]){2,}[a-z0-9]+$/i` | Correspond à un nom d'utilisateur avec au moins deux segments séparés par des tirets ou underscores. |
| `/^[A-Z][a-z]+\s[A-Z][a-z]+\s[A-Z][a-z]+$/` | Correspond à un nom complet avec un prénom, un deuxième prénom et un nom de famille. |
| `/^(\d{5}-\d{4}\|\d{5})$/` | Correspond à un code postal américain, avec ou sans le suffixe de 4 chiffres. |
| `/^\d{2}/\d{2}/\d{4}$/` | Correspond à une date au format MM/DD/YYYY. |
| `/^\d{2}/\d{2}/\d{2}$/` | Correspond à une date au format MM/DD/YY. |

## Exemples d'utilisation en PHP

Voici quelques exemples montrant comment utiliser les expressions régulières dans PHP avec la fonction `preg_match` :

*   `preg_match('/^\d+$/', '12345'); ` Retourne 1 si la chaîne est composée uniquement de chiffres
*   `preg_match('/^[a-zA-Z]+$/', 'HelloWorld'); ` Retourne 1 si la chaîne est composée uniquement de lettres
*   `preg_match('/^[a-z0-9_]+$/i', 'abc_123'); ` Retourne 1 pour une chaîne de lettres, chiffres et underscores
*   `preg_match('/^(\d{4})-(\d{2})-(\d{2})$/', '2024-09-09'); ` Retourne 1 pour une date au format YYYY-MM-DD
*   `preg_match('/^\S+@\S+\.\S+$/', 'example@example.com'); `Retourne 1 pour une adresse email simple
*   `preg_match('/^(https?:\/\/)?([a-z0-9\-\.]+)\.([a-z]{2,6})(\/[\w\.-]*)*\/?$/i', 'https://example.com/path'); ` Retourne 1 pour une URL
*   `preg_match('/^(\+?\d{1,4}[\s-])?(?!0+\s,?\d)([2-9]\d{2}[\s-]?\d{3}[\s-]?\d{4})(\s?(x|ext)\d{1,5})?$/', '+1-123-456-7890 ext123'); ` Retourne 1 pour un numéro de téléphone avec extension
*   `preg_match('/^\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2}$/', '2024-09-09 14:30:00'); ` Retourne 1 pour une date et une heure au format YYYY-MM-DD HH:MM:SS
*   `preg_match('/^(?=.*[A-Za-z])(?=.*\d)[A-Za-z\d]{8,}$/', 'Password1'); ` Retourne 1 pour un mot de passe contenant au moins une lettre, un chiffre, et ayant au moins 8 caractères





```
<?php
// Définir une expression régulière pour vérifier une adresse email
$emailPattern = '/^[\w\.-]+@[\w\.-]+\.\w+$/';

// Chaîne à tester
$email = 'test@example.com';

// Vérifier si l'adresse email est valide
if (preg_match($emailPattern, $email)) {
    echo "L'adresse email '$email' est valide.";
} else {
    echo "L'adresse email '$email' n'est pas valide.";
}
?>
```

Dans cet exemple :

*   L'expression régulière `'/^[\w\.-]+@[\w\.-]+\.\w+$/'` vérifie que la chaîne de texte est une adresse email simple.
*   `preg_match` est utilisé pour comparer la chaîne `$email` avec l'expression régulière définie dans `$emailPattern`.
