# Adoption-Website

### Motivation
This was a project to test our understand of using javascript functions to print data to the DOM. We completed in a group of four, but all writing our own code. We also figured out how to use Event Listeners and to sort the adoption cards by specific categories

### Build Status
complete.

### Code Style
We used HTML5, Javascript and CSS3

### Screenshots

![Screen Shot 2020-07-24 at 2 57 43 PM](https://user-images.githubusercontent.com/66916708/88492365-ee075980-cf6f-11ea-9ea6-b703120be371.jpg)


![Screen Shot 2020-07-26 at 6 44 46 PM](https://user-images.githubusercontent.com/66916708/88492388-1bec9e00-cf70-11ea-9324-d606b9100f2f.png)

### Features
I use event listeners at the top of the page so that the user has the option to sort by dogs, cats, dinos or put all the adoption options back on the page

### Code Example

```// Dino Button
const buildAdoptionCardsDino = () => {
  domString = "";
  for (let i = 0; i < pets.length; i++) {
    if (pets[i].type === "dino") {
      domString += `<div class="card">`;
      domString += `<div class="name">`;
      domString += `<h2>${pets[i].name}</h2>`;
      domString += `</div>`;
      domString += `<div>`;
      domString += `<img class="image" src=${pets[i].imageUrl} alt="dino pic"/>`;
      domString += `<p class="color">${pets[i].color}</p>`;
      domString += `<p class="specialskill">${pets[i].specialSkill}</p>`;
      domString += `</div>`;
      domString += `<div class="pushToBottom">`;
      domString += `<h3 class="typeOfAnimal-${pets[i].type}">${pets[i].type}</h3>`;
      domString += `</div>`;
      domString += `</div>`;
    }
    printToDom("animal-cards", domString);
  }
};

document
  .getElementById("button-1")
  .addEventListener("click", buildAdoptionCardsDog);
```
### Website Link
https://adoptioncards.netlify.app/
