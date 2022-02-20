# Linux commands


## grep lines before and after matched line

``` title="alice.txt"
Alice sits on a riverbank on a warm summer day, 
drowsily reading over her sister’s shoulder, 
when she catches sight of a White Rabbit in a waistcoat running by her. 
The White Rabbit pulls out a pocket watch, 
exclaims that he is late, and pops down a rabbit hole. 
Alice follows the White Rabbit down the hole and comes upon a great hallway lined with doors. 
She finds a small door that she opens using a key she discovers on a nearby table. 
Through the door, she sees a beautiful garden, 
and Alice begins to cry when she realizes she cannot fit through the door. 
She finds a bottle marked “DRINK ME” and downs the contents.
```

* Just want to find ```waistcoat``` in ```alice.txt```
```shell
$ grep waistcoat alice.txt
when she catches sight of a White Rabbit in a waistcoat running by her. 
```

* If you want 1 line Before the matched line,
```shell
$ grep -B1 waistcoat alice.txt
drowsily reading over her sister’s shoulder,
when she catches sight of a White Rabbit in a waistcoat running by her. 
```

* If you want 2 lines After the matched line,
```shell
$ grep -A2 waistcoat alice.txt
when she catches sight of a White Rabbit in a waistcoat running by her.
The White Rabbit pulls out a pocket watch,
exclaims that he is late, and pops down a rabbit hole.
```
 