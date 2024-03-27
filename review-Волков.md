1. Ну уровень конечно желательно доделать
```
method void makeGrid() {
        var Array cells;
        var Cell cell;
        var int k;
```
2. Это бы вынести в отдельный метод
```
while (i < rows) {
            let j = 0;
            while (j < cols) {
                let index = (i * cols) + j;
                let cells[index] = Cell.new(i, j, size, start);
                let j = j + 1;
            }
            
            let i = i + 1;
        }
```

3. Тут поправил, можно обращаться на прямую к полю, а не засовывать в локальную переменную
```
while(i < (rows*cols)) {
			do cells[i].dispose();
			let i = i + 1;
```

4. Тут забыл класс убрать из памяти
```
do Grid.deAlloc(this);
```