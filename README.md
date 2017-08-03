# Missing Number in Array with Javascript
Missing Number in Array using Javascript

Fork missing_number_array.js for code
You can use test.html to test code if you need to.

// Missing Number in Array  
var a= [1,2,3,4,5,7,8,9,10];

//var a = [1,4,2,7];
var missing = [];

a.sort(function (a, b){return a - b;});

for (var i = 0; i<a.length; i++){
    
    if (a[i] - a[i-1] != 1){
        
        var next = a[i] - a[i-1];
        
        var counter = 1;
        
        while(counter<next){
            
            missing.push(a[i-1]+counter);
            
            counter++;
            
        }
    }
}


for (var i = 0; i<missing.length; i++){
    
    console.log("Missing Number = " + missing[i]);
    
    document.write("Missing Number = " + missing[i] + "<br />");
    
} 
