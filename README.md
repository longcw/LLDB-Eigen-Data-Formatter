# LLDB Eigen Data Formatter

LLDB Data Formatter for dense matrices and vectors of the [Eigen](http://eigen.tuxfamily.org) library.

## Example

```cpp
Eigen::Matrix<double, 3, 3> A;
A << 1, 0, 0,
	 0, 2, 0,
	 0, 0, 3;
```

Corresponding output in LLDB

```
(lldb) print A
(Eigen::Matrix<double, 3, 3, 0, 3, 3>) $11 = rows: 3, cols: 3
[ 1 0 0;
  0 2 0;
  0 0 3 ]
```

## Installation

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/longcw/LLDB-Eigen-Data-Formatter/master/tools/install.sh)"
```

__Manual Installation__

```bash
INSTALL_PATH=~/.lldb-eigen-data-formatter
git clone https://github.com/longcw/LLDB-Eigen-Data-Formatter.git $INSTALL_PATH
echo 'command script import "'$INSTALL_PATH'/LLDB_Eigen_Data_Formatter.py"' >> ~/.lldbinit
```

__Uninstallation__

```bash
rm -fr ~/.lldb-eigen-data-formatter
```

Afterwards remove the `command script import` command in `~/.lldbinit`.

## License

Copyright © 2016 Till Ehrengruber

Distributed under the GNU GENERAL PUBLIC LICENSE.

## Opencv Formatter
https://github.com/longcw/LLDB-Opencv-Data-Formatter