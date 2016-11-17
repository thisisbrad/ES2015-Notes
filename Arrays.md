// FOR EACH 
var images = [
  { height: 10, width: 30 },
  { height: 20, width: 90 },
  { height: 54, width: 32 }
];
var areas = [];
function calc (image) {
   var total = image.height * image.width;
   areas.push(total);
}
images.forEach(calc);

// MAP 
var paints = [ { color: 'red' }, { color: 'blue' }, { color: 'yellow' }];

function pluck(array, property) {
    var data = array.map(function(item){
        return item[property]
    })
    return data
}

pluck(paints, 'color');

// FILTER 
var users = [
 { id: 1, admin: true },  
 { id: 2, admin: false },
 { id: 3, admin: false },
 { id: 4, admin: false },
 { id: 5, admin: true },
];

var filteredUsers = users.filter(function(user){
	return user.admin;
});

var numbers = [10, 20, 30];

function reject(array, iteratorFunction) {
  return array.filter(function(number){
    return !iteratorFunction(number);
  });
}

var lessThanFifteen = reject(numbers, function(number){
  return number > 15;
}); 

lessThanFifteen;

// FIND 
var users = [
  { id: 1, admin: false },
  { id: 2, admin: false },
  { id: 3, admin: true }
];

var admin = users.find(function(user){
    return user.admin;
});

var ladders = [
  { id: 1, height: 20 },
  { id: 3, height: 25 }
];

function findWhere(array, criteria) {
  var property = Object.keys(criteria);
  var ladder = array.find(function(item){
      return item[property] === criteria[property];
  });
  return ladder;
}

findWhere(ladders, { gfgdf: '20' });

// EVERY && SOME 
var users = [
  { id: 21, hasSubmitted: true },
  { id: 62, hasSubmitted: false },
  { id: 4, hasSubmitted: true }
];

var hasSubmitted = users.every(function(user){
    return user.hasSubmitted;
});

var requests = [
  { url: '/photos', status: 'complete' },
  { url: '/albums', status: 'pending' },
  { url: '/users', status: 'failed' }
];

var inProgress = requests.some(function(req){
    return req.status === 'pending';
});

var totalDistance = trips.reduce(function(totalDistance, trip){
    return total += trip.distance;
},0);

// use find to find current number in array
// if it finds a result there is a double of that number
// so if not a double push it in right away
// if it is a double check if it's in 

```
return array.reduce(function(previous, element){
  let inPrevious = previous.find(function(inPrevious){
     return inPrevious === element;
  });
  if (!inPrevious) {
      previous.push(element);
  }
      return previous;
}, []);
```
//for React and .createClass it's a between using composition over inheritance. Using .createClass isn't bad because it's not OOP or ES6. It's still a valid way to write a React class. The developers just picked between creating classes using the factory pattern or the constructor pattern basically, which are both "classes" either way .  This article has a better insight on React.Component vs React.createClass (it's from 2015 I know that's ancient in the React timeline lol)
//https://reactjsnews.com/composing-components













