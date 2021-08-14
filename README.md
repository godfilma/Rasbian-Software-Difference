# Rasbian-Software-Difference
A list of packages that appear in "raspios_full_armhf" but not in "raspios_armhf" both the 2021-05-07 releases.
  On the website, these are called "Raspberry Pi OS with desktop and recommended software" and "Raspberry Pi OS with desktop", respectively.

## Reading the data
Download the .txt and open it in any text editor or into Microsoft Excel or LibreOffice Calc, or any other spreadsheet maker that can import fixed-width text.

## Recreation Process:
I grabbed the .info files from:
  https://downloads.raspberrypi.org/raspios_full_armhf/images/raspios_full_armhf-2021-05-28/
  https://downloads.raspberrypi.org/raspios_armhf/images/raspios_armhf-2021-05-28/

Then, I imported them into LibreOffice Calc as fixed-width data (this can also be done in Microsoft Excel).
  I selected the shorter column of packages (the one without recommended software) and defined it as a range.
  Then, next to the recommended-software column, I used the command MATCH(<cell of recommended software>,Defined_Range_Name,0) to define every row with a match.
  Rows without matches had errors.
  Then, I sorted the data by the MATCH column, so that all the errors were in one location. Finally, I deleted all the matched data, leaving only the packages that were in the "Full" release but not in the regular one.
  Finally, I exported the data as a fixed-width .csv file.
