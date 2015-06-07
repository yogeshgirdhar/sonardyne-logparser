# sonardyne-logparser
Takes in sonardyne USBL generated log files, and outputs location of tracked vehicles in CSV format.


# Usage
```
$sonardyne_parse <UTM zone number> <UTM zone letter> <output.csv> sonardynelogfile1.csv [sonardynelogfile2.csv ..]
```
for example, if you have a folder containing the following logfiles: [20150505.csv, 20150505_0.csv, 20150505_1.csv], with data collected in Panama (zone 17N), then you can run the code in the following way:

```
$sonardyne_parse  17 n parsed.csv 20150505*.csv
```
This will put the parsed location of the tracked vehicles in parsed.csv file. The output might look something like this:

```
...
2015-04-05 13:30:52.478,LATLON,NADIR 2705,7.41947554798,-82.1248557356,-196.288135186
2015-04-05 13:30:57.478,LATLON,NADIR 2705,7.41949356315,-82.1248545972,-196.302148814
2015-04-05 13:30:57.478,LATLON,NADIR 2705,7.41949330587,-82.1248540729,-196.260984244
2015-04-05 13:31:02.478,LATLON,NADIR 2705,7.41952244894,-82.1248582532,-196.963561816
...
```
Here 'NADIR 2705' was the name of the tracked vehicle, the the corresponding numbers are lat, lon, depth

#License
The MIT License (MIT)

Copyright (c) 2015 Yogesh Girdhar <yogi@whoi.edu>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
