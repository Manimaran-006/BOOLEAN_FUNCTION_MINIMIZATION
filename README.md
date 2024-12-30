## NAME:V.MANIMARAN
## REG NO:24008541
# EXPERIMENT2:BOOLEAN FUNCTION MINIMIZATION
# AIM:

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
# EQUIPMENT REQUIRED:

Hardware – PCs, Cyclone II , USB flasher

# SOFTWARE - QUARTUS PRIME

# THEORY
# THEORY OF BOOLEAN FUNCTION MINIMIZATION

Boolean function minimization involves simplifying Boolean expressions without changing their output. This is essential in digital circuit design, as it leads to more efficient implementations with fewer logic gates and reduced complexity.

# KEY CONCEPTS

1. # BOOLEAN FUNCTIONS:
   - Functions that map binary inputs to binary outputs (0 or 1).
   - Can be represented in various forms: truth tables, algebraic expressions, and logic diagrams.

2. # CANONICAL FORMS:
   - Sum of Products (SOP): Expresses the function as a sum (OR) of products (ANDs), with each product term corresponding to a minterm.
   - Product of Sums (POS): Expresses the function as a product (AND) of sums (ORs), with each sum term corresponding to a maxterm.

3. # MINTERMS AND MAXTERMS:
   - Minterm: A product term that represents a single combination of inputs that outputs 1.
   - Maxterm: A sum term that represents a single combination of inputs that outputs 0.

# MINIMIZATION TECHNIQUES

1. ## KARNAUGH MAPS (K-MAPS):
   - A visual method for simplifying Boolean expressions.
   - Organizes truth values in a grid, allowing for the identification of groups of adjacent cells (1s for SOP, 0s for POS) to combine terms and eliminate variables.

2. # QUINE-MCCLUSKEY ALGORITHM:
   - A systematic, tabular approach for minimizing Boolean functions, especially useful for functions with many variables.
   - Steps include listing minterms, grouping them, combining terms to find prime implicants, and selecting essential prime implicants.

3. # PRIME IMPLICANTS:
   - A prime implicant is a product term that cannot be further simplified.
   - Essential prime implicants are those that cover at least one minterm not covered by other prime implicants.

# PROPERTIES OF BOOLEAN ALGEBRA

- # IDEMPOTENT LAW: \( A + A = A \), \( A \cdot A = A \)
- # DOMINANCE LAW: \( A + 1 = 1 \), \( A \cdot 0 = 0 \)
- # COMPLEMENT LAW: \( A + \overline{A} = 1 \), \( A \cdot \overline{A} = 0 \)
- # DISTRIBUTIVE, ASSOCIATIVE, AND COMMUTATIVE LAWS: Used for algebraic simplifications and to manipulate expressions.

# CONCULSION

The theory of Boolean function minimization is vital for creating efficient digital circuits. By employing techniques like K-maps and the Quine-McCluskey algorithm, designers can simplify complex functions, leading to reduced resource usage and improved performance in electronic systems.
# TRUTH TABLE
![Screenshot (74)](https://github.com/user-attachments/assets/613321a9-db96-45f6-ae00-4becd7a622ac)

# PROCEDURE

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.![Uploading Screenshot (74).png…]()


5.	For different input combinations generate the timing diagram.


# PROGRAM:

module booleanfunction(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
assign x1=(~a)&(~b)&(~c)&(~d);
assign x2=(a)&(~c)&(~d);
assign x3=(~b)&(c)&(~d);
assign x4=(~a)&(b)&(c)&(d);
assign x5=(b)&(~c)&(d);
assign x6=(~w)&(~x)&(~y)&(~z);
assign x7=(w)&(~y)&(~z);
assign x8=(~x)&(y)&(~z);
assign x9=(~w)&(x)&(y)&(z);
assign x10=(x)&(~y)&(z);
assign F1=x1|x2|x3|x4|x5;
assign F2=x6|x7|x8|x9|x10;
endmodule


# RTL OUTPUT:
![Screenshot (55)](https://github.com/user-attachments/assets/c2495f04-8a25-429d-858a-c632e6aeaaa8)


# OUTPUT WAVEFORM:
![Screenshot (60)](https://github.com/user-attachments/assets/1e51b948-05f3-4413-8927-1f9274bcd85d)


# RESULT:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

