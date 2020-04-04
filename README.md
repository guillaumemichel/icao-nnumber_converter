# ICAO – N-Number Converter

Script converting ICAO addresses to N-Numbers (Tail Numbers) and reciprocally. Only works for United States aircraft registrations.

## Running the script

### Requirements

- Python 3.x
- Nothing else =)

### Install

Simply clone the repo, and start converting.

```bash
git clone https://github.com/guillaumemichel/icao-nnumber_converter.git
cd icao-nnumber_converter
```

### Usage

Convert N-Number to ICAO address
```bash
> python convert.py N12345
a061d9
```

Convert ICAO address to N-Number
```bash
> python convert.py abcdef
N86QU
```

## Format & Mapping

ICAO addresses are hexadecimal values of length 6. US registered ICAO addresses start with 'a'. N-Numbers, or Tail Numbers, are alphanumerical strings at most 6 characters long. US registered Tail Numbers start with 'N' (that's why they are called N-Number, yes!). Their format is as defined below.

There is a direct sequential mapping from US ICAO addresses to N-Number, from a00001 for N1 to adf7c7 for N99999. The mapping is somewhat intuitive, but not convenient to implement.

The mapping goes like this:

| ICAO address | N-Number |
|--------------|----------|
| a00001       | N1       |
| a00002       | N1A      |
| a00003       | N1AA     |
| a00004       | N1AB     |
| a00005       | N1AC     |
| ...          | ...      |
| a0001a       | N1AZ     |
| a0001b       | N1B      |
| a0001c       | N1BA     |
| a0001d       | N1BB     |
| ...          | ...      |
| a00259       | N1ZZ     |
| a0025a       | N10      |
| a0025b       | N10A     |
| a0025c       | N10AA    |
| a0025d       | N10AB    |
| ...          | ...      |
| a004b2       | N10ZZ    |
| a004b3       | N100     |
| a004b4       | N100A    |
| a004b5       | N100AA   |
| a004b6       | N100AB   |
| ...          | ...      |
| a0070b       | N100ZZ   |
| a0070c       | N1000    |
| a0070d       | N1000A   |
| a0070e       | N1000B   |
| ...          | ...      |
| a00724       | N1000Z   |
| a00725       | N10000   |
| a00726       | N10001   |
| a00727       | N10002   |
| ...          | ...      |
| a0072e       | N10009   |
| a0072f       | N1001    |
| a00730       | N1001A   |
| a00731       | N1001B   |
| ...          | ...      |
| a00751       | N10019   |
| a00752       | N1002    |
| ...          | ...      |
| a00869       | N10099   |
| a0086a       | N101     |
| a0086b       | N101A    |
| a0086c       | N101AA   |
| ...          | ...      |
| a00c20       | N10199   |
| a00c21       | N102     |
| a00c22       | N102A    |
| ...          | ...      |
| a029d8       | N10999   |
| a029d9       | N11      |
| a029da       | N11A     |
| a029db       | N11AA    |
| ...          | ...      |
| a05157       | N11999   |
| a05158       | N12      |
| ...          | ...      |
| a18d4f       | N19999   |
| a18d50       | N2       |
| a18d51       | N2A      |
| a18d52       | N2AA     |
| ...          | ...      |
| a31a9e       | N29999   |
| a31a9f       | N3       |
| ...          | ...      |
| ac6a79       | N9       |
| ac6a7a       | N9A      |
| ...          | ...      |
| adf7c7       | N99999   |


## Useful links:
- This [forum post](https://discussions.flightaware.com/t/n-number-icao-address/18009).
- [FAA N-Number Inquiry](https://registry.faa.gov/aircraftinquiry/NNum_Inquiry.aspx)
