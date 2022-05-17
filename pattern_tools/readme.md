## Readme

**Usage**: 

`python gen_pattern.py --help`

to generate various calibration svg calibration patterns.

**Examples**:

create a checkerboard pattern in file chessboard.svg with 9 rows, 6 columns and a square size of 20mm: 

```shell
python gen_pattern.py -o chessboard.svg --rows 9 --columns 6 --type checkerboard --square_size 20
```

create a circle board pattern in file circleboard.svg with 7 rows, 5 columns and a radius of 15mm: 

```shell
python gen_pattern.py -o circleboard.svg --rows 7 --columns 5 --type circles --square_size 15
```

create a circle board pattern in file acircleboard.svg with 7 rows, 5 columns and a square size of 10mm and less spacing between circle: 

```shell
python gen_pattern.py -o acircleboard.svg --rows 7 --columns 5 --type acircles --square_size 10 --radius_rate 2
```

create a radon checkerboard for [findChessboardCornersSB()](https://docs.opencv.org/4.x/d9/d0c/group__calib3d.html#gadc5bcb05cb21cf1e50963df26986d7c9) with markers in (7 4), (7 5), (8 5) cells: 

```shell
python gen_pattern.py -o radon_checkerboard.svg --rows 10 --columns 15 --type radon_checkerboard -s 12.1 -m 7 4 7 5 8 5
```

If you want to change unit use -u option (mm inches, px, m)

If you want to change page size use -w and -h options

## Web Resources:

- https://docs.opencv.org/4.x/da/d0d/tutorial_camera_calibration_pattern.html
