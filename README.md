# wilks

_Jupyter notebook to fit a reciprocal polynomial on Wilks coefficients_

The Wilks coefficients are used to compare the weights lifted by athletes of different body weights.
The weight lifted is multiplied by a coefficient according to the body weight.
The higher the product, the better the athlete has performed.

Unfortunately, the creator of the formula, Robert Wilks, CEO of Powerlifting Australia,
hasn't published the formula on which the coefficients are based on.
Only two tables of coefficients are [available](https://powerliftingaustralia.com/wilks-formula/), one for men, one for women.

The code in this Jupyter notebook extracts the coefficients from those tables (see the files wilks-men.tsv and wilks-women.tsv) and fits a reciprocal polynomial on them:

_coeff = g / (a + b⋅x + c⋅x<sup>2</sup> + d⋅x<sup>3</sup> + e⋅x<sup>4</sup> + f⋅x<sup>5</sup>)_

Where _x_ is the athlete's body weight and the independent parameters _a_, _b_, _c_, … _g_ are to optimized to fit the curve to the given coefficients.

It turns out that the following values make the formula almost perfectly fit the coefficients:

|     | Men              | Women            |
| --- | ---------------- | ---------------- |
| _a_ | 3.63670138e+04   | -9.31498570e+04  |
| _b_ | 6.55937783e+03   | 1.01904268e+04   |
| _c_ | 5.65741690e+01   | -2.43239016e+01  |
| _d_ | -1.07472551e+00  | -7.84945613e-01  |
| _e_ | 5.45052301e-03   | 7.00489691e-03   |
| _f_ | -9.30455617e-06  | -1.74074520e-05  |
| _g_ | 4.63384381e+05   | 4.46372497e+05   |


## License

Copyright &copy; 2020 [Oliver Lau](mailto:oliver@ersatzworld.net)

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see [http://www.gnu.org/licenses/](http://www.gnu.org/licenses/).