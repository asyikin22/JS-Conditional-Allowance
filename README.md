# Conditional task with two choices

This script automates a simple allowance system based on whether the checkbox is clicked; representing chores being done. The steps are explained below:

**Step1** - Initializing variables:
* Select first input element: checkBox using document.querySelector
* Select p element using document.querySelector
* Initializes a variable choresDone = chores has not been done yet

**Step 2** - Event Listener for checkbox change:
* This line adds an event listener to checkbox element ---> checkBox.addEventListener('change', () => { ... }); 
* Inside function 
 	* checkBox.disabled = true; ---> this disables checkbox after clicking it to prevent multiple clicks
	* choresDone = true; ---> chores are done
	* updateAllowance(); ---> this calls the function to calculate and display the allowance

**Step 3** - Update Allowance function
* let childsAllowance; ---> declares a variable to store the calculated allowance
* If Else function checks the value of choresDone
   * If true, sets allowance to 20
   * If false, sets allowance to 10
* Para.textContent ---> update the text content of element with a message displaying the earned allowance amount


**Step 4** - Calling updateAllowance initially
* updateAllowance(); ---> this calls the function ONCE when the script loads and ensures the initial allowance message is displayed even if the checkbox has not been clicked yet
