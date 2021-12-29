# sat 

## Install and Use
From Github:
```
git clone https://github.com/rcpatrick/sat.git
```
From my website:
```
git clone git://git.raypatrick.xyz/sat.git
```
Then:
```
cd sat
sudo make install
```

## NAME

sat - Retrieves near-real-time NOAA GOES weather satellite imagery. 

## SYNOPSIS

`sat SITE IMAGERY_PRODUCT [-i] [-u]`


## DESCRIPTION

sat is a tool that searches for imagery of a slice of the Western hemisphere as viewed by the GOES-East and GOES-West satellites, then retrieves one of 5 different imagery products: black & white infrared, color infrared, visible light, water vapor, or a composite of water vapor and black & white infrared.

## OPTIONS

`SITE`

:	GOES satellites really image an entire hemisphere at once, but weather information customers are usually interested in smaller regions. The full-disk GOES image is divided into slices centered on certain geographical regions or features. SITE is the geographical region or feature that the view is centered on. May be one of the following:
:		abq	Albuquerque, NM
:		ak	Alaska
:		alb	Albany, NY
:		aus	Austin, TX
:		bwi	Baltimore, MD
:		carib	Caribbean
:		clt	Charlotte, NC
:		cod	Yellowstone
:		den	Denver, CO
:		dtw	Detroit, MI
:		evv	Evansville, ID
:		gulf	Gulf of Mexico
:		hi	Hawaii
:		ict	Wichita, KS
:		las	Las Vegas, NV
:		lit	Little Rock, AR
:		lws	Leniston, ID
:		mgm	Montgomery, AL
:		msp	Minneapolis, MN
:		pir	Pierre, SD
:		tpa	Tampa, FL
:		wmc	Winnemacca, NV
:		us	Contiguous United States

`IMAGERY_PRODUCT`

:	GOES satellites have instruments that collect across several spectral bands in both visible light and infrared. IMAGERY_PRODUCT specifies which spectral band you want to see imagery from. May be one of the following:
:		irbw	Infrared (black & white)
:		ircol	Infrared (color)
:		irnws	Composite of infrared and water vapor
:		vis	Visible light (site must be in daylight)
:		wv	Water vapor

`-i,--interactive`

:	Requires `dmenu(1).` Allows interactive fuzzy-search input rather than manually typing sites and imagery codes.

`-u,--url`

:	Just print the URL of the image to stdout rather than opening it with mpv.

## BUGS

Report any bugs to ray@raypatrick.xyz.

## AUTHOR

Written 2021 by Ray Patrick.

## SEE ALSO

`dmenu(1)`
