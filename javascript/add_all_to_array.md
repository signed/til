const all = ['one', 'two'];
const addition = ['three', 'four'];
const special_addition = { 0:"five", 1: "six", "length": 2};


Array.prototype.push.apply(all, addition);
all.push.apply(all, special_addition);
console.log(all);
