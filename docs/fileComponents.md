#### <a name="file/FileSaver.java"></a> file/FileSaver.java

This java class handles the file writing process.

- Global variables:
  - fw:
    - type: `FileWriter`
	- accessModifier: private
	- description: used to open or create file and write to it
- Functions:
  - FileSaver:
    - type: constructor
	- accessModifier: public
	- description: opens or create a file in append mode, filename: output.jsonl
  - FileSaver:
    - type: constructor
	- accessModifier: public
	- parameters:
	  - fileName:
	    - type: `String`
	- description: opens or create a file in append mode, filename: name given as argument
  - write:
    - type: general function
	- accessModifier: public
	- returnType: `boolean`
	- parameters:
	  - mt:
	    - type: `Metrics`
	- description: write to a file and returns status
  - close:
    - type: general function
	- accessModifier: public
	- returnType: `void`
	- description: close the opened file