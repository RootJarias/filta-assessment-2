# Excercise 2

```
Library/Technology Used:

- Tailwind CSS: I've used tailwind CSS for utility classes. (https://tailwindcss.com/)
- Daisy UI: Used for tailwind code enchancements. (https://daisyui.com/)
- Pinia: Used for state management.
- Auto Animate: To add a animation between elements that moved.
```

## Instructions

#### 1.) Go to the path of the chosen excercise then insall the needed dependencies.

```
cd excercise-2

npm install
```

#### 2.) To run the project simply do:

```
npm run serve
```

===

## Explain why the result of ('b' + 'a' + + 'a' + 'a').toLowerCase() is banana.

```
+ 'a' becomes a NaN ("Not a Number") value because it force string to a number, while the character a cannot be parsed as a number. so It became Banana.
You can also try by removing the ".toLowerCase()" to see the difference (expectation: 'baNaNa')
```

## Notes:

#### Data files is located in `/assets/files/data.json`
