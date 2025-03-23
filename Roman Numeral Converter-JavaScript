const numberInput = document.getElementById("number");
const convertBtn = document.getElementById("convert-btn");
const output = document.getElementById("output");

const numberToRoman = (input) =>{
  const valueSymbols = [[1000, "M"], [900, "CM"], [500, "D"], [400, "CD"], [100, "C"], [90, "XC"], [50, "L"], [40, "XL"], [10, "X"], [9, "IX"], [5, "V"], [4, "IV"], [1, "I"]];
  const resultArr = [];
  for(const [value,roman] of valueSymbols){
    while(input>=value){
      input -= value;
      resultArr.push(roman);
    }
    if(input===0){
      break;
    }
  }
  return output.textContent = resultArr.join("");
}

const checkUserInput = () =>{
  const inputVal = Number(numberInput.value);

  if(!inputVal || isNaN(inputVal)){
    return output.textContent = "Please enter a valid number";
  } 

  if(inputVal<=0){
    return output.textContent = "Please enter a number greater than or equal to 1";
  }

  if(inputVal>3999){
    return output.textContent = "Please enter a number less than or equal to 3999";
  }

  output.textContent = numberToRoman(inputVal);
  numberInput.value = "";
}

convertBtn.addEventListener("click", checkUserInput);

numberInput.addEventListener("keydown", (e) => {
  if (e.key === "Enter") {
    checkUserInput();
  }
});
