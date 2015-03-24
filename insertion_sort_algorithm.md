##Insertion Sort Algorithm
Insertion sort always maintains two zones in the array to be sorted: sorted and unsorted.
At the beginning the sorted zone consist of one element (the first element of array that we are sorting).
On each step the algorithms expand the sorted zone by one element inserting the first element from the unsorted zone in the proper place in the sorted zone and shifting all larger elements one slot down.<br>
<ul>Pros
<li>Efficient for small data sets</li>
<li>Can sort a list while it recieves it</li>
</ul>
<ul>Cons
<li>Much less efficient on large lists</li>
<li></li>
</ul><br>
######Example<br>
This algorithm is not something uncommon to the persons who know card playing. In the game of cards, a player gets 13 cards. He keeps them in the sorted order in his hand for his ease. A player looks at the first two cards, sorts them and keeps the smaller card first and then the second. Suppose that two cards were 9 and 8, the player swap them and keep 8 before 9. Now he takes the third card. Suppose, it is 10, then it is in its position. If this card is of number 2, the player will pick it up and put it on the start of the cards. Then he looks at the fourth card and inserts it in the first three cards (that he has sorted) at a proper place. He repeats the same process with all the cards and finally gets the cards in a sorted order. Thus in this algorithm, we keep the left part of the array sorted and take element from the right and insert it in the left part at its proper place. Due to this process of insertion, it is called insertion sorting.<br>
######Ruby Example<br>
```
def  insertionsort(num)
for j in 1..num.length
	key = num[j]
	i = j - 1
	while i > 0 and num[i] > key
		num[i+1] = num[i]
		i = i - 1
	end
	num[i+1] = key
end	
puts num
end

numbers = [23,34,46,87,12,1,66]
insertionsort(numbers)
```
######Javascript Example<br>
```
function sort(values) {
  var length = values.length;
  for(var i = 1; i < length; ++i) {
    var temp = values[i];
    var j = i - 1;
    for(; j >= 0 && values[j] > temp; --j) {
      values[j+1] = values[j];
    }
    values[j+1] = temp;
  }
};
sort([7, 4, 5, 2, 9, 1]);
```
