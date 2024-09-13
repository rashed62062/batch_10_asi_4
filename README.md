
 

function calculateTax(income,expense){


    if (income <= 0 || expense <= 0 || expense > income){
       return "Invalid Input"
    }
         
       let profit = income - expense;
       let tax = profit * 0.20;
       
       return tax;
       
    }

    


function sendNotification(email){

    let nameEmail = email.split("@");
    
    if(nameEmail.length!=2){
        return "Invalid Input"
    }

    let name = nameEmail [0];
    let userName = nameEmail[1];
    
    let result = `${name} I send you can email ${userName}`
    return result;
}
   const result =  sendNotification("nadim.naem5@outlook.com");

   console.log(result);



function checkDigitsInName(name){
    if(typeof name!='string'){
           return "invalid input"
       }
       for(let i=0;i<name.length;i++){
           if (name[i] >= '0' && name[i] <= '9') {
               return true;
           }
       }
   
       return false;
   
   }
   

   function calculateFinalScore(studentInfo) {

    if (typeof studentInfo !== 'object' || studentInfo === null ||
        typeof studentInfo.name !== 'string' || 
        typeof studentInfo.testScore !== 'number' || 
        typeof studentInfo.schoolGrade !== 'number' || 
        typeof studentInfo.isFFamily !== 'boolean') {
        return "Invalid Input";
    }


    if (studentInfo.testScore > 50 || studentInfo.testScore < 0 ||
        studentInfo.schoolGrade > 30 || studentInfo.schoolGrade < 0) {
        return "Invalid Input";
    }

    
    let finalScore = studentInfo.testScore + studentInfo.schoolGrade;


    if (studentInfo.isFFamily) {
        finalScore += 20;
    }


    return finalScore >= 80;
}
   




function waitingTime(waitingTimes, serialNumber) {
    


    if (!Array.isArray(waitingTimes) || typeof serialNumber !== 'number') {
        return "Invalid Input";
    }

    

    let totalTime = 0;
    let numberOfPeople = waitingTimes.length;

    for (let time of waitingTimes) {
        totalTime += time;
    }

    
    let averageTime = Math.round(totalTime / numberOfPeople);

    
    let peopleRemaining = serialNumber - 1 - numberOfPeople;


    if (peopleRemaining <= 0) {
        return 0;
    }

    let isratWaitingTime = peopleRemaining * averageTime;
    return isratWaitingTime;
}
