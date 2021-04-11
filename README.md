JustBasic is a BASIC interpreter for Raspberry PI PICO RP2040
=============================================================

State of work:
- the project is targetted for both PICO and Windows (used mostly as development platform now)
- the supported features are described in the manual folder; relevant examples can be found in examples folder
- the binary for PICO is compiled with 'no_flash' flag - just drag & drop the uf2 file, start putty and press enter
- aimed to support most BASIC features in modern way: INT / FLOAT / STRING, arrays (now single dimension for INT / FLOAT), GOSUB & GOTO to use labels instead of line numbers, FOR / NEXT & WHILE loops and IF / THEN / ELSE / ENDIF with nesting, DATA / READ, PAUSE / GETTICK, complex expressions; complex logical expressions, build-in command tracing, built-in editor, flexible code formatting (non line oriented), many build in functions including string processing, and many others

Blinky example
==============
	REM Led-pin 25

	pmode 25, 1

	for k=1 to 10 step 0

		pause 500
	
		dwrite 25,1
	
		pause 500
	
		dwrite 25,0
	
	next k

	end

General example
===============
	PRINT "IF/THEN/ELSE/ENDIF"
	a=0
	WHILE a <= 10
		IF a%2 = 1 THEN 
			PRINT "odd" 
			PRINT a 
		ELSE 
			PRINT "even ", a 
		ENDIF
		a=a+1
	ENDWHILE
---
Bogdan Golab
