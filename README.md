```javascript
let priceInput = document.querySelectorAll(".price-input input");
let RangeInput = document.querySelectorAll(".range-input input");
let slider = document.querySelector(".price-slider");
let priceGap = 500;

for (let i = 0; i < RangeInput.length; i++) {
    RangeInput[i].addEventListener("input", () => {
        let minRange = parseInt(RangeInput[0].value);
        let maxRange = parseInt(RangeInput[1].value);
        let diff = maxRange - minRange;
        priceInput[0].value = minRange;
        priceInput[1].value = maxRange;

    })
}

for (let i = 0; i < priceInput.length; i++) {
    priceInput[i].addEventListener("input", () => {
        let minPrice = parseInt(priceInput[0].value);
        let maxPrice = parseInt(priceInput[1].value);
        RangeInput[0].value = minPrice;
        RangeInput[1].value = maxPrice;

    })
}
```
