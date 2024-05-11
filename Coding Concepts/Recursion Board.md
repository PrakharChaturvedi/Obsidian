---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
How function calls works in languages ^70Y96MPr

-> Now main function is always in stack
memory until the execution of all operation
is completed.

-> if a function is calling another function,
the function calling the other function 
stays in the stack.... This can work as a 
hierarchy, with main function being the root 
node of the whole hierarchy.
  ^ISxifkxI

# While the function is not finished
executing it remains in stack ^dI6iCisV

# When a function finished executing 
it is removed from the stack and 
returns the flow of program
is restored to where the function was 
called ^P3jKJ9sp

main ^5GqsIW0a

print1 (1) ^UHNNEySd

print2 (2) ^pGiX8u76

print4 (4) ^UHSlshny

print3 (3) ^rJQESOa5

print5 (5) ^sIkju25D

order of removal from stack ^UJaDSCff

order of function calling  ^raeNhRC9

Stack Diagram : ^npFLpPuP

1 ^SVvj27Th

2 ^HhGimhxq

What is Recursion ^ChsdGppt

# Recursion is nothing but a condition 
in which a function calls itself... ^mKAysLFV

# In recursion their must be a check 
condition or base condition 
for stopping the function from 
calling itself when the 
requirement is completed.   ^TcZyPgAO

CODE Example : 
    public static void main(String[] args) {
        print(1);
    }    

    static void print(int n){
        if(n == 5){
            System.out.println(n);
            return;
        }
        System.out.println(n);
        print(n+1);
    } ^btlP4EgF

main ^XafBksFh

print1 (1) ^4L3RXsJP

print2 (2) ^JEmSLaV8

print4 (4) ^oP8Ij74R

print3 (3) ^NsqZtrOM

print5 (5) ^9iuGjqpg

order of removal from stack ^DvRSyD1U

order of function calling  ^yYl1xnVm

Stack Diagram : ^SqHwDiEr

base condition ^CeM1a88z

recursive call ^1z2c4tyd

# If you are calling a function again and again,
you can treat it as a separate call in the stack ^QFwuJA2d

# As u call a function again and again it will 
take memory separately in Stack Memory ^1a7kixeI

# No base condition -> Function calls will keep 
happening, stack will be filled again and again 
and each function consumes some memory --->
 ^jEBkCGx3

# Resulting in Stack over flow error,
i.e. Memory limit of computer is exceeded. ^DhJgnLdf

 Why Recursion ^To6v9dZy

3 ^mbEmtmf8

# It helps us in solving bigger/ complex
problems in a simple way. ^tKSjNyXD

# You can convert recursion solutions into 
iteration and vice versa, once converted
iterations it becomes optimized  ^YSbyKERU

-> It is also easier to solve complex problems
using recursion so it's a great first step in 
solving a problem....  ^6yVoIW2g

-> Space complexity : It is not constant because
of recursive calls. ^TxDuQZNE

-> It helps in breaking down bigger problems 
into smaller problems ^79kOHO8n

Visualizing Recursion : ^yu1MDIC3

main () ^7HGTrOiH

print (1) ^RaD1usPH

print (2) ^4XJ3Boq8

print (3) ^SRdkoDIp

print (4) ^rOZzSNwb

print (5) ^cn1XWncT

Program
Over ^U6Kzw9k7

// This diagram
is known as 
Recursive Tree ^LyGcLhlW

Fibonacci numbers using recursion ^DNKZSKoz

Fibo(5) ^WqlkSe2X

Fibo(4) ^UX7QwdfA

Fibo(0) ^kXZteN4C

Fibo(2) ^NyBxbw9W

Fibo(3) ^fV5D8vUn

Fibo(1) ^HuFvZxkG

Fibo(0) ^TOamhdZm

Fibo(2) ^ZEE8NWeo

Fibo(1) ^8HHPw7A5

Fibo(1) ^MsnKKE0m

Fibo(3) ^nlUeiZer

Fibo(1) ^T0yj9shF

Fibo(0) ^ep74lFcS

Fibo(2) ^4LCBMfXH

Fibo(1) ^WC4FbLX7

# First break the problem down 
into smaller problems... ^CGwrF2pi

Fibo(n) = fibo(n-1) + fibo(n-2) ^bBELOlAN

# When you write recursion in a 
formula it is termed as recurrent 
relation ^65GiPJfv

-> The base condition is regarded by
answers we already have  ^lEcGNk4Z

For Example: In this case we already know that F(0) = 0 and F(1) = 1 ^mSTGfb0Z

# We were able to identify that this was an question which can be solved with the help of 
recursion as we knew the base conditions and was able to break the problems into
multiple smaller problems. ^34hy3u6q

4 ^4GId5vda

fig : Recursive tree for Fibonacci numbers  ^PsEsPDne

Code Vault path: "C:\IDK\Java\Recursion\..." ^GnCI0LkM

Same as 
Others ^k6N3kdm5

 How to understand and approach a problem  ^N5xzVXeM

# Identify if you can break down problem into 
smaller problems ^YneffLUi

# Write down recurrent relation if needed ^jnwLVCBt

# Draw the recursive tree ^SbOdzVSu

# About the tree :-
-> See the flow of functions, how they 
are getting in stack ...
-> Identify the flow of left and right 
tree calls ... ^42HSEtpP

# See how th e values are returned at each step.
See where two function call will come out of, In the 
end you will come out of the main function ... ^GuVLaSAY

Follow these steps to 
solve any recursion problem  ^peCeEojF

5 ^sRA96vkQ

Binary Search ^TN1Dffvn

# F(N) = O(1) + F(N/2) ^eV7Fd9dP

6 ^0SxsfI4O

Recursive realtion ^GmQ3DVLb

Comparison time ^5LuaFveO

Dividing array
in half ^P1u6XiAt

 # if you want to apply binary search on 
an array of size n, take a step that takes 
constant amount of time + search in 
half of the array  ^DxLatxQR

Types of recurrent relations : ^0egKluFl

(1) Linear recurrent relations : Fibonacci num
(2) Divide and conquer : Binary search
(Returned by a factor)  ^LU3lD7mv

    static int search(int[] arr, int target, int s, int e){
        if (s > e){
            return -1;
        }
        int m = s + (e-s)/2;

        if(arr[m] == target){
            return m;
        }
        if(target < arr[m]){
            search(arr, target, s, m-1);
        }
        return search(arr, target, m+1, e);
    } ^vnNOtLsk

arguments ^LwvxQsum

finding middle 
elements ^8i30woIx

Base Conditions and
recursive calls ^r8qOaHjW

Leet Code questions solved till now ^Ro7Qpx0I

# 1
# 2
# 3
# 4
# 5 ^JKE5NDE6

Merge Sort ^a0iCYkPB

7 ^qh6DrQAZ

 7, 3, 2, 16, 24, 4, 11, 9 ^4ILq2TAn

 7, 3, 2, 16 ^72slPVrg

24, 4, 11, 9 ^Ia7puK6b

7, 3 ^cdSvUd8Y

2, 16 ^elbz5VuB

24, 4 ^Uy87kZSf

11, 9 ^pNbB4b8r

7 ^Ycn4qRLV

3 ^vXrF2yaA

2 ^b3OeVAYl

16 ^g8KTCoJ1

24 ^SRAiTKTK

4 ^TXchz12K

11 ^IutFOYDx

9 ^FiQNYPt9

3, 7 ^rDk0XVXv

2, 16 ^4uRDHRrY

4, 24 ^ywbtldX4

9, 11 ^v0KhnzWs

2, 3, 7, 16 ^mClnaHph

4, 9, 11, 24 ^WZtS9Lwe

2, 3, 4, 7, 9, 11, 24 ^NwbVqlrk

Steps : 
(1) Divide away into parts
(2) Get both parts sorted via recursion
(3) Merge the sorted parts ^ndV7AkyU

Explanation point 3 :  ^iSKSP0Ei

arr1 = [2, 3, 7, 16] ^4tsQygCN

arr2 = [4, 9, 11, 24] ^hzJp4Por

Sorted Array = [2, 3, 4, 7, 9, 11, 16, 24] ^ELEWsBMc

Time Complexity : O(nLogn) ^B5g5t86d

Space Complexity : O(n) ^IV7SiSjZ

Quick Sort ^QyoEyPdR

8 ^hVb1ogJm

[ 10, 80, 30, 90, 40, 50, 70 ] ^ZvROuNCQ

[ 10, 30, 40, 50 ] ^C1r57hJF

[ 90, 80 ] ^fTJqV4MM

[ 10, 30, 40 ] ^0N8Un32r

[ ] ^wNV0U12M

[ 10, 30 ] ^AtlrsqaH

[ ] ^0JsKTmEn

[ 10 ] ^VR3wLF4i

[ ] ^FQMQdXOY

[ 90] ^uZvmjxiM

[ ] ^yA6rhPSq

pivot ^cqcgUhMi

# How to pick the pivot element :
- Random element
- Corner element
- middle element ^lqbbIqc9

Notes :
- Not stable
- In-plane
- Merge Sort is better for linked list
    due to memory allocation of linked
    list is not continuous.  ^mZwLE2pl

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.1.3",
	"elements": [
		{
			"type": "line",
			"version": 1424,
			"versionNonce": 884900573,
			"isDeleted": false,
			"id": "ZMpA0lMMPb_OALGG4TfdT",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -194.6254001031907,
			"y": -161.55908961133954,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.827622986267201,
			"height": 266.8268557847768,
			"seed": 314333224,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158210,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					-1.827622986267201,
					266.8268557847768
				]
			]
		},
		{
			"type": "line",
			"version": 1484,
			"versionNonce": 1585800563,
			"isDeleted": false,
			"id": "iqPNhp21otz39j0-fhUwb",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 4.3672102545272935,
			"y": -165.550413652221,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.827622986267201,
			"height": 266.8268557847768,
			"seed": 1557074728,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158210,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					-1.827622986267201,
					266.8268557847768
				]
			]
		},
		{
			"type": "line",
			"version": 1163,
			"versionNonce": 1124343613,
			"isDeleted": false,
			"id": "ccNrHHkaBJOkW80-7G6Tf",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -197.36679972424733,
			"y": 104.35398953864774,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 199.20637391837926,
			"height": 2.741329904368209,
			"seed": 1792175656,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158210,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					199.20637391837926,
					2.741329904368209
				]
			]
		},
		{
			"type": "text",
			"version": 791,
			"versionNonce": 1983790867,
			"isDeleted": false,
			"id": "70Y96MPr",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -632.2127931305606,
			"y": -332.2562086312111,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 512.7637939453125,
			"height": 35,
			"seed": 296759128,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158210,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "How function calls works in languages",
			"rawText": "How function calls works in languages",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "How function calls works in languages",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1576,
			"versionNonce": 1125592989,
			"isDeleted": false,
			"id": "ISxifkxI",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -639.4215650011809,
			"y": -68.9669308812305,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 346.5758361816406,
			"height": 200,
			"seed": 1458226984,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158210,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "-> Now main function is always in stack\nmemory until the execution of all operation\nis completed.\n\n-> if a function is calling another function,\nthe function calling the other function \nstays in the stack.... This can work as a \nhierarchy, with main function being the root \nnode of the whole hierarchy.\n ",
			"rawText": "-> Now main function is always in stack\nmemory until the execution of all operation\nis completed.\n\n-> if a function is calling another function,\nthe function calling the other function \nstays in the stack.... This can work as a \nhierarchy, with main function being the root \nnode of the whole hierarchy.\n ",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "-> Now main function is always in stack\nmemory until the execution of all operation\nis completed.\n\n-> if a function is calling another function,\nthe function calling the other function \nstays in the stack.... This can work as a \nhierarchy, with main function being the root \nnode of the whole hierarchy.\n ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 658,
			"versionNonce": 15393971,
			"isDeleted": false,
			"id": "dI6iCisV",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -656.6332327464659,
			"y": -251.4633745316944,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 278.2718505859375,
			"height": 40,
			"seed": 698667608,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158210,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# While the function is not finished\nexecuting it remains in stack",
			"rawText": "# While the function is not finished\nexecuting it remains in stack",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# While the function is not finished\nexecuting it remains in stack",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 851,
			"versionNonce": 53031933,
			"isDeleted": false,
			"id": "P3jKJ9sp",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -672.4705039743834,
			"y": -185.20496310897224,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 311.1358337402344,
			"height": 100,
			"seed": 1516959528,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# When a function finished executing \nit is removed from the stack and \nreturns the flow of program\nis restored to where the function was \ncalled",
			"rawText": "# When a function finished executing \nit is removed from the stack and \nreturns the flow of program\nis restored to where the function was \ncalled",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# When a function finished executing \nit is removed from the stack and \nreturns the flow of program\nis restored to where the function was \ncalled",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 992,
			"versionNonce": 103929427,
			"isDeleted": false,
			"id": "U3Fb8btJ97HBJFmhZhYHj",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -690.7140016112547,
			"y": -376.14918139778996,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 810.7795986610721,
			"height": 542.2523373967291,
			"seed": 953055320,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false
		},
		{
			"type": "freedraw",
			"version": 687,
			"versionNonce": 255568989,
			"isDeleted": false,
			"id": "dU7JkM129Q0sD_cljeu0x",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -197.08769793911128,
			"y": 65.0084923739634,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 195.56254758710438,
			"height": 1.9914717237998616,
			"seed": 19952424,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.39828826727057276
				],
				[
					1.194895189258716,
					-0.39828826727057276
				],
				[
					1.99147172379989,
					-0.39828826727057276
				],
				[
					3.9829434475997516,
					-0.39828826727057276
				],
				[
					5.57612690412904,
					-0.39828826727057276
				],
				[
					9.16078208445819,
					-0.39828826727057276
				],
				[
					13.94030206659906,
					-0.39828826727057276
				],
				[
					19.51642897072807,
					0
				],
				[
					24.295979340315938,
					0
				],
				[
					29.075499322456807,
					0
				],
				[
					34.253337959315246,
					0
				],
				[
					39.82943447599732,
					0
				],
				[
					48.59192829318491,
					0
				],
				[
					54.964631731855064,
					0.7965765345411455
				],
				[
					62.133942092513365,
					0.7965765345411455
				],
				[
					69.30322206572473,
					0.7965765345411455
				],
				[
					76.47253242638303,
					0.7965765345411455
				],
				[
					83.64181239959439,
					0.7965765345411455
				],
				[
					90.41283449298211,
					0.7965765345411455
				],
				[
					97.58211446619342,
					0.7965765345411455
				],
				[
					103.95484829231057,
					0.7965765345411455
				],
				[
					110.32755173098073,
					0.7965765345411455
				],
				[
					115.90367863510974,
					0.7965765345411455
				],
				[
					121.08148688452124,
					0.7965765345411455
				],
				[
					125.8610372541091,
					0.7965765345411455
				],
				[
					129.84398070170883,
					0.7965765345411455
				],
				[
					135.02178895112027,
					0.7965765345411455
				],
				[
					137.41154894219076,
					0.7965765345411455
				],
				[
					141.792811044508,
					1.5931834565292888
				],
				[
					144.18257103557843,
					1.5931834565292888
				],
				[
					146.9706192939195,
					1.5931834565292888
				],
				[
					149.36037928498993,
					1.5931834565292888
				],
				[
					152.5467461980485,
					1.5931834565292888
				],
				[
					154.1399296545778,
					1.5931834565292888
				],
				[
					156.52968964564823,
					1.5931834565292888
				],
				[
					157.72458483490695,
					1.5931834565292888
				],
				[
					158.12287310217752,
					1.5931834565292888
				],
				[
					159.7160565587068,
					1.5931834565292888
				],
				[
					160.91092136051853,
					1.5931834565292888
				],
				[
					161.3092096277891,
					1.5931834565292888
				],
				[
					163.30068135158902,
					1.5931834565292888
				],
				[
					163.69900000630653,
					1.5931834565292888
				],
				[
					164.89386480811825,
					1.5931834565292888
				],
				[
					166.08875999737697,
					1.5931834565292888
				],
				[
					166.48704826464754,
					1.5931834565292888
				],
				[
					168.4785199884474,
					1.5931834565292888
				],
				[
					169.2750965229886,
					1.5931834565292888
				],
				[
					170.46999171224726,
					1.5931834565292888
				],
				[
					171.66488690150598,
					1.5931834565292888
				],
				[
					172.85975170331776,
					1.5931834565292888
				],
				[
					173.25803997058833,
					1.5931834565292888
				],
				[
					174.05464689257641,
					1.5931834565292888
				],
				[
					174.45293515984704,
					1.5931834565292888
				],
				[
					175.2495116943882,
					1.5931834565292888
				],
				[
					175.6478303491057,
					1.5931834565292888
				],
				[
					176.04611861637633,
					1.5931834565292888
				],
				[
					176.84269515091748,
					1.5931834565292888
				],
				[
					177.24098341818805,
					1.5931834565292888
				],
				[
					178.0375903401762,
					1.5931834565292888
				],
				[
					178.43587860744677,
					1.5931834565292888
				],
				[
					179.2324551419879,
					1.5931834565292888
				],
				[
					179.63077379670548,
					1.5931834565292888
				],
				[
					180.02906206397606,
					1.5931834565292888
				],
				[
					180.8256385985172,
					1.5931834565292888
				],
				[
					181.22392686578777,
					1.5931834565292888
				],
				[
					182.02053378777592,
					1.5931834565292888
				],
				[
					183.21539858958764,
					1.5931834565292888
				],
				[
					183.6137172443052,
					1.5931834565292888
				],
				[
					184.80858204611692,
					1.5931834565292888
				],
				[
					185.2068703133875,
					1.5931834565292888
				],
				[
					186.00347723537564,
					1.5931834565292888
				],
				[
					186.8000537699168,
					1.5931834565292888
				],
				[
					187.59666069190493,
					1.5931834565292888
				],
				[
					187.9949489591755,
					1.5931834565292888
				],
				[
					189.18981376098722,
					1.5931834565292888
				],
				[
					189.98642068297536,
					1.5931834565292888
				],
				[
					190.38470895024594,
					1.5931834565292888
				],
				[
					190.7829972175165,
					1.5931834565292888
				],
				[
					191.57960413950465,
					1.5931834565292888
				],
				[
					191.97789240677523,
					1.5931834565292888
				],
				[
					192.77446894131637,
					1.5931834565292888
				],
				[
					193.172757208587,
					1.5931834565292888
				],
				[
					193.9693641305751,
					1.5931834565292888
				],
				[
					194.36765239784566,
					1.5931834565292888
				],
				[
					194.76594066511623,
					1.5931834565292888
				],
				[
					195.56254758710438,
					1.5931834565292888
				],
				[
					195.56254758710438,
					1.5931834565292888
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 673,
			"versionNonce": 1424593907,
			"isDeleted": false,
			"id": "guV4SpnG11HKcBieOK99n",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -196.68937928439374,
			"y": 33.04536512948616,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 202.3335089055982,
			"height": 2.3897599910704344,
			"seed": 834573864,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.7965765345411455
				],
				[
					0,
					-1.1948648018117183
				],
				[
					0.7965765345411739,
					-1.1948648018117183
				],
				[
					1.1948648018117467,
					-1.1948648018117183
				],
				[
					1.99147172379989,
					-1.1948648018117183
				],
				[
					2.7880482583410355,
					-1.1948648018117183
				],
				[
					3.9829434475997516,
					-1.1948648018117183
				],
				[
					5.177808249411498,
					-1.5931834565292888
				],
				[
					7.567568240481933,
					-2.3897599910704344
				],
				[
					13.541983411881517,
					-2.3897599910704344
				],
				[
					15.93177379039895,
					-2.3897599910704344
				],
				[
					22.70276549633968,
					-2.3897599910704344
				],
				[
					28.278892400468692,
					-2.3897599910704344
				],
				[
					33.855019304597704,
					-2.3897599910704344
				],
				[
					40.22772274326792,
					-2.3897599910704344
				],
				[
					46.600426181938076,
					-2.3897599910704344
				],
				[
					52.97312962060823,
					-2.3897599910704344
				],
				[
					60.142439981266534,
					-2.3897599910704344
				],
				[
					66.51514341993675,
					-2.3897599910704344
				],
				[
					73.68445378059505,
					-2.3897599910704344
				],
				[
					80.0571572192652,
					-2.3897599910704344
				],
				[
					85.63328412339422,
					-2.3897599910704344
				],
				[
					91.20938064007629,
					-2.3897599910704344
				],
				[
					95.98893100966416,
					-2.3897599910704344
				],
				[
					99.5735861899933,
					-2.3897599910704344
				],
				[
					102.75992271560489,
					-2.3897599910704344
				],
				[
					105.14968270667532,
					-2.3897599910704344
				],
				[
					106.74286616320461,
					-2.3897599910704344
				],
				[
					107.93776135246333,
					-2.3897599910704344
				],
				[
					110.32752134353376,
					-2.3897599910704344
				],
				[
					110.72580961080439,
					-2.3897599910704344
				],
				[
					111.52241653279248,
					-2.3897599910704344
				],
				[
					111.92070480006305,
					-2.3897599910704344
				],
				[
					112.31899306733362,
					-2.3897599910704344
				],
				[
					113.11556960187482,
					-2.3897599910704344
				],
				[
					113.51388825659234,
					-2.3897599910704344
				],
				[
					114.31046479113354,
					-2.3897599910704344
				],
				[
					115.5053599803922,
					-2.3897599910704344
				],
				[
					117.09851304947455,
					-2.3897599910704344
				],
				[
					119.88659169526255,
					-2.3897599910704344
				],
				[
					122.67463995360356,
					-1.9914717237998616
				],
				[
					126.25929513393271,
					-1.9914717237998616
				],
				[
					127.852478590462,
					-1.9914717237998616
				],
				[
					132.2337103053323,
					-1.5931834565292888
				],
				[
					135.42007721839087,
					-1.5931834565292888
				],
				[
					139.80130893326117,
					-1.5931834565292888
				],
				[
					143.7842523808609,
					-1.5931834565292888
				],
				[
					149.3603792849899,
					-1.5931834565292888
				],
				[
					154.93647580167197,
					-1.5931834565292888
				],
				[
					160.512602705801,
					-1.5931834565292888
				],
				[
					166.08872960993,
					-0.7965765345411455
				],
				[
					172.4614330486002,
					-0.7965765345411455
				],
				[
					178.03755995272923,
					-0.7965765345411455
				],
				[
					183.21539858958766,
					-0.7965765345411455
				],
				[
					187.1983420371874,
					-0.7965765345411455
				],
				[
					191.97786201932826,
					-0.7965765345411455
				],
				[
					195.5625171996574,
					-0.7965765345411455
				],
				[
					198.74885372526904,
					-0.7965765345411455
				],
				[
					199.94374891452776,
					-0.7965765345411455
				],
				[
					200.34203718179833,
					-0.7965765345411455
				],
				[
					201.13864410378642,
					-0.7965765345411455
				],
				[
					201.536932371057,
					-0.7965765345411455
				],
				[
					202.3335089055982,
					-0.7965765345411455
				],
				[
					201.93522063832762,
					0
				],
				[
					201.536932371057,
					0
				],
				[
					200.7403254490689,
					0
				],
				[
					200.34203718179833,
					0
				],
				[
					199.54546064725713,
					0
				],
				[
					199.14717237998656,
					0
				],
				[
					199.14717237998656,
					-0.39828826727057276
				],
				[
					198.74885372526904,
					-0.39828826727057276
				],
				[
					198.74885372526904,
					-0.7965765345411455
				],
				[
					198.74885372526904,
					-0.7965765345411455
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 701,
			"versionNonce": 1998592189,
			"isDeleted": false,
			"id": "pbKqVETYaPrFuUvxTKIqd",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -194.69790756059385,
			"y": -4.394309355440697,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 194.36762201039872,
			"height": 1.5931834565292888,
			"seed": 467697448,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.39828826727057276,
					0
				],
				[
					1.5931530690823195,
					0
				],
				[
					2.7880482583410355,
					0
				],
				[
					4.381231714870324,
					0
				],
				[
					5.974415171399556,
					0
				],
				[
					8.364175162470048,
					0
				],
				[
					11.550511688081627,
					0
				],
				[
					15.53345513568135,
					0
				],
				[
					19.914717237998644,
					0
				],
				[
					24.694237220139513,
					0
				],
				[
					30.270364124268525,
					0
				],
				[
					36.64306756293874,
					0
				],
				[
					43.81237792359704,
					0
				],
				[
					50.98165789680834,
					0
				],
				[
					59.34583305927842,
					0.39831865471757055
				],
				[
					66.51514341993672,
					0.39831865471757055
				],
				[
					76.47250203893603,
					0.39831865471757055
				],
				[
					85.63328412339419,
					1.194895189258716
				],
				[
					93.20085236387612,
					1.194895189258716
				],
				[
					101.56505791379314,
					1.194895189258716
				],
				[
					107.14115443047521,
					1.194895189258716
				],
				[
					110.72580961080436,
					1.194895189258716
				],
				[
					113.1155696018748,
					1.194895189258716
				],
				[
					115.10704132567466,
					1.194895189258716
				],
				[
					115.90364824766274,
					1.194895189258716
				],
				[
					117.09851304947452,
					1.194895189258716
				],
				[
					117.89511997146266,
					1.194895189258716
				],
				[
					118.29340823873324,
					1.194895189258716
				],
				[
					119.08998477327438,
					1.194895189258716
				],
				[
					119.4883034279919,
					1.194895189258716
				],
				[
					121.08145649707424,
					1.5931834565292888
				],
				[
					122.67463995360353,
					1.5931834565292888
				],
				[
					125.06439994467397,
					1.5931834565292888
				],
				[
					127.05587166847383,
					1.5931834565292888
				],
				[
					129.84395031426183,
					1.5931834565292888
				],
				[
					134.6234702964027,
					1.5931834565292888
				],
				[
					139.00470201127305,
					1.5931834565292888
				],
				[
					141.39449238979043,
					1.5931834565292888
				],
				[
					143.78425238086086,
					1.5931834565292888
				],
				[
					144.97911718267264,
					1.5931834565292888
				],
				[
					145.77572410466078,
					1.5931834565292888
				],
				[
					146.9705889064725,
					1.5931834565292888
				],
				[
					148.16548409573122,
					1.5931834565292888
				],
				[
					148.96206063027236,
					1.5931834565292888
				],
				[
					149.36037928498993,
					1.5931834565292888
				],
				[
					149.7586675522605,
					1.5931834565292888
				],
				[
					150.55524408680165,
					1.5931834565292888
				],
				[
					150.95353235407222,
					1.5931834565292888
				],
				[
					151.75013927606037,
					1.5931834565292888
				],
				[
					152.14842754333094,
					1.5931834565292888
				],
				[
					153.34332273258966,
					1.5931834565292888
				],
				[
					153.74161099986023,
					1.5931834565292888
				],
				[
					155.7330827236601,
					1.5931834565292888
				],
				[
					157.32626618018938,
					1.5931834565292888
				],
				[
					158.91941924927167,
					1.5931834565292888
				],
				[
					161.3092096277891,
					1.5931834565292888
				],
				[
					162.90236269687145,
					1.5931834565292888
				],
				[
					164.8938344206713,
					1.5931834565292888
				],
				[
					166.4870178772006,
					1.5931834565292888
				],
				[
					168.08020133372983,
					1.5931834565292888
				],
				[
					169.27509652298855,
					1.5931834565292888
				],
				[
					170.46996132480032,
					1.5931834565292888
				],
				[
					171.66485651405898,
					1.5931834565292888
				],
				[
					172.46143304860018,
					1.5931834565292888
				],
				[
					173.25803997058827,
					1.5931834565292888
				],
				[
					173.6563282378589,
					1.5931834565292888
				],
				[
					174.45290477240005,
					1.5931834565292888
				],
				[
					174.85119303967062,
					1.5931834565292888
				],
				[
					175.64779996165876,
					1.5931834565292888
				],
				[
					176.04608822892934,
					1.5931834565292888
				],
				[
					176.4443764961999,
					1.5931834565292888
				],
				[
					177.24098341818805,
					1.5931834565292888
				],
				[
					177.63927168545862,
					1.5931834565292888
				],
				[
					178.43584821999977,
					1.5931834565292888
				],
				[
					178.83413648727034,
					1.5931834565292888
				],
				[
					179.63074340925849,
					1.5931834565292888
				],
				[
					180.02903167652906,
					1.5931834565292888
				],
				[
					180.42731994379963,
					1.5931834565292888
				],
				[
					181.22392686578777,
					1.5931834565292888
				],
				[
					181.62221513305835,
					1.5931834565292888
				],
				[
					182.4187916675995,
					1.5931834565292888
				],
				[
					182.81707993487007,
					1.5931834565292888
				],
				[
					183.21539858958764,
					1.5931834565292888
				],
				[
					184.01197512412878,
					1.5931834565292888
				],
				[
					184.41026339139935,
					1.5931834565292888
				],
				[
					185.60515858065807,
					1.5931834565292888
				],
				[
					186.8000233824698,
					1.5931834565292888
				],
				[
					187.19834203718736,
					1.5931834565292888
				],
				[
					187.9949185717285,
					1.5931834565292888
				],
				[
					188.39320683899908,
					1.5931834565292888
				],
				[
					189.18981376098722,
					1.5931834565292888
				],
				[
					189.5881020282578,
					1.5931834565292888
				],
				[
					190.78296683006957,
					1.5931834565292888
				],
				[
					191.18128548478708,
					1.5931834565292888
				],
				[
					191.97786201932823,
					1.5931834565292888
				],
				[
					192.3761502865988,
					1.5931834565292888
				],
				[
					193.17275720858694,
					1.5931834565292888
				],
				[
					193.57104547585752,
					1.5931834565292888
				],
				[
					194.36762201039872,
					1.5931834565292888
				],
				[
					193.9693337431281,
					1.5931834565292888
				],
				[
					193.9693337431281,
					1.5931834565292888
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 705,
			"versionNonce": 488152467,
			"isDeleted": false,
			"id": "ZRLpTa6WcXEDOz1vbWrgq",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -193.50304275878213,
			"y": -47.01179208977902,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 194.36765239784566,
			"height": 2.788048258341007,
			"seed": 2044640296,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.194895189258716,
					0
				],
				[
					2.3897599910704628,
					0
				],
				[
					3.584655180329179,
					0
				],
				[
					4.779550369587838,
					0
				],
				[
					5.57612690412904,
					0
				],
				[
					7.567598627928902,
					0
				],
				[
					9.16078208445819,
					0.39828826727057276
				],
				[
					10.75396554098748,
					0.39828826727057276
				],
				[
					12.34711861006977,
					0.39828826727057276
				],
				[
					14.338590333869632,
					0.39828826727057276
				],
				[
					15.931773790398921,
					0.39828826727057276
				],
				[
					18.321533781469412,
					0.39828826727057276
				],
				[
					20.711324159986788,
					0.39828826727057276
				],
				[
					23.499372418327795,
					0.39828826727057276
				],
				[
					25.889132409398286,
					0.39828826727057276
				],
				[
					29.473787589727436,
					0.39828826727057276
				],
				[
					31.86354758079787,
					0.39828826727057276
				],
				[
					34.651626226585876,
					0.39828826727057276
				],
				[
					36.64309795038574,
					0.39828826727057276
				],
				[
					40.22772274326789,
					0.39828826727057276
				],
				[
					43.015801389055895,
					0.39828826727057276
				],
				[
					46.20213791466753,
					0.39828826727057276
				],
				[
					48.59192829318491,
					0.39828826727057276
				],
				[
					51.379976551525914,
					0.39828826727057276
				],
				[
					53.769736542596405,
					0.39828826727057276
				],
				[
					56.956103455654926,
					0.39828826727057276
				],
				[
					59.74415171399599,
					0.39828826727057276
				],
				[
					62.93051862705457,
					0.39828826727057276
				],
				[
					66.11685515266615,
					0.39828826727057276
				],
				[
					70.49811725498344,
					0.39828826727057276
				],
				[
					74.48106070258316,
					0.39828826727057276
				],
				[
					78.06568549546537,
					0.39828826727057276
				],
				[
					81.2520524085239,
					0.39828826727057276
				],
				[
					84.43841932158247,
					0.39828826727057276
				],
				[
					86.82817931265296,
					0.39828826727057276
				],
				[
					89.61622757099397,
					0.39828826727057276
				],
				[
					92.0059875620644,
					0.39828826727057276
				],
				[
					93.5991710185937,
					0.39828826727057276
				],
				[
					95.98893100966413,
					0.39828826727057276
				],
				[
					97.58211446619342,
					0.39828826727057276
				],
				[
					98.77700965545213,
					0.39828826727057276
				],
				[
					99.97187445726385,
					0.39828826727057276
				],
				[
					101.56505791379314,
					0.39828826727057276
				],
				[
					102.75995310305186,
					0.39828826727057276
				],
				[
					103.95481790486363,
					0.39828826727057276
				],
				[
					105.54800136139286,
					0.39828826727057276
				],
				[
					106.74289655065158,
					0.39828826727057276
				],
				[
					109.13265654172201,
					0.39828826727057276
				],
				[
					110.7258399982513,
					0.39828826727057276
				],
				[
					112.31902345478059,
					0.39828826727057276
				],
				[
					114.31049517858045,
					0.39828826727057276
				],
				[
					116.30196690238031,
					0.39828826727057276
				],
				[
					118.29343862618018,
					0.39828826727057276
				],
				[
					120.68319861725067,
					0.39828826727057276
				],
				[
					122.27638207377996,
					0.39828826727057276
				],
				[
					124.66614206485039,
					0.39828826727057276
				],
				[
					126.25932552137968,
					0.39828826727057276
				],
				[
					128.6490855124501,
					0.39828826727057276
				],
				[
					130.2422689689794,
					0.39828826727057276
				],
				[
					132.63202896004984,
					0.39828826727057276
				],
				[
					134.22521241657913,
					0.39828826727057276
				],
				[
					136.61497240764956,
					0.39828826727057276
				],
				[
					139.8013089332612,
					1.1948951892586877
				],
				[
					144.18257103557843,
					1.1948951892586877
				],
				[
					152.14845793077794,
					1.1948951892586877
				],
				[
					153.34332273258966,
					1.1948951892586877
				],
				[
					155.7330827236601,
					1.1948951892586877
				],
				[
					159.71602617125987,
					1.9914717237998616
				],
				[
					163.6989696188596,
					1.9914717237998616
				],
				[
					167.28362479918874,
					1.9914717237998616
				],
				[
					170.46999171224726,
					1.9914717237998616
				],
				[
					173.25803997058833,
					1.9914717237998616
				],
				[
					175.2495116943882,
					1.9914717237998616
				],
				[
					176.4444068836469,
					1.9914717237998616
				],
				[
					177.24098341818805,
					1.9914717237998616
				],
				[
					178.0375903401762,
					1.9914717237998616
				],
				[
					178.43587860744677,
					1.9914717237998616
				],
				[
					179.2324551419879,
					1.9914717237998616
				],
				[
					179.63074340925849,
					1.9914717237998616
				],
				[
					180.42735033124663,
					1.9914717237998616
				],
				[
					180.8256385985172,
					1.9914717237998616
				],
				[
					181.22392686578777,
					2.3897599910704344
				],
				[
					182.02053378777592,
					2.3897599910704344
				],
				[
					182.4188220550465,
					2.3897599910704344
				],
				[
					183.21539858958764,
					2.3897599910704344
				],
				[
					183.6136868568582,
					2.3897599910704344
				],
				[
					184.01200551157578,
					2.3897599910704344
				],
				[
					184.80858204611692,
					2.3897599910704344
				],
				[
					185.2068703133875,
					2.3897599910704344
				],
				[
					186.00347723537564,
					2.3897599910704344
				],
				[
					186.4017655026462,
					2.3897599910704344
				],
				[
					187.19834203718736,
					2.3897599910704344
				],
				[
					187.59663030445793,
					2.3897599910704344
				],
				[
					187.9949489591755,
					2.3897599910704344
				],
				[
					188.79152549371665,
					2.3897599910704344
				],
				[
					189.18981376098722,
					2.3897599910704344
				],
				[
					190.38470895024594,
					2.3897599910704344
				],
				[
					191.18128548478708,
					2.788048258341007
				],
				[
					191.5795737520577,
					2.788048258341007
				],
				[
					191.97789240677523,
					2.788048258341007
				],
				[
					192.77446894131637,
					2.788048258341007
				],
				[
					193.172757208587,
					2.788048258341007
				],
				[
					193.9693641305751,
					2.788048258341007
				],
				[
					194.36765239784566,
					2.788048258341007
				],
				[
					194.36765239784566,
					2.788048258341007
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 706,
			"versionNonce": 1417148701,
			"isDeleted": false,
			"id": "14RwsSeWJOGaDwLiRJoMX",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -194.69790756059385,
			"y": -87.23953002677041,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 192.77443855386943,
			"height": 1.1948799955352172,
			"seed": 1938670888,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7965765345411455,
					0
				],
				[
					1.1948648018117183,
					0
				],
				[
					2.3897599910704344,
					0
				],
				[
					3.9829434475996948,
					-0.7965765345411455
				],
				[
					5.974415171399556,
					-0.7965765345411455
				],
				[
					7.567568240481904,
					-1.1948799955352172
				],
				[
					9.160751697011193,
					-1.1948799955352172
				],
				[
					11.550511688081627,
					-1.1948799955352172
				],
				[
					16.330062057669494,
					-1.1948799955352172
				],
				[
					21.109582039810363,
					-1.1948799955352172
				],
				[
					25.490813754680715,
					-1.1948799955352172
				],
				[
					31.066940658809727,
					-1.1948799955352172
				],
				[
					36.64306756293874,
					-1.1948799955352172
				],
				[
					43.81237792359704,
					-1.1948799955352172
				],
				[
					50.98165789680834,
					-1.1948799955352172
				],
				[
					58.150968257466644,
					-1.1948799955352172
				],
				[
					66.51514341993672,
					-1.1948799955352172
				],
				[
					74.48103031513617,
					-1.1948799955352172
				],
				[
					82.44691721033561,
					-1.1948799955352172
				],
				[
					90.01451583826454,
					-1.1948799955352172
				],
				[
					97.18379581147585,
					-1.1948799955352172
				],
				[
					103.556529637593,
					-1.1948799955352172
				],
				[
					109.92923307626316,
					-1.1948799955352172
				],
				[
					117.89511997146266,
					-1.1948799955352172
				],
				[
					119.4883034279919,
					-1.1948799955352172
				],
				[
					122.67463995360353,
					-1.1948799955352172
				],
				[
					123.86953514286225,
					-1.1948799955352172
				],
				[
					124.26782341013282,
					-1.1948799955352172
				],
				[
					125.06439994467397,
					-1.1948799955352172
				],
				[
					125.46271859939154,
					-1.1948799955352172
				],
				[
					126.25929513393268,
					-1.1948799955352172
				],
				[
					126.65758340120325,
					-1.1948799955352172
				],
				[
					127.85247859046197,
					-1.1948799955352172
				],
				[
					129.0473433922737,
					-1.1948799955352172
				],
				[
					130.64052684880298,
					-1.1948799955352172
				],
				[
					132.23371030533227,
					-1.1948799955352172
				],
				[
					134.22518202913213,
					-1.1948799955352172
				],
				[
					135.81836548566142,
					-1.1948799955352172
				],
				[
					137.4115489421907,
					-1.1948799955352172
				],
				[
					139.00470201127305,
					-1.1948799955352172
				],
				[
					140.99617373507292,
					-1.1948799955352172
				],
				[
					142.5893571916022,
					-1.1948799955352172
				],
				[
					144.1825406481315,
					-1.1948799955352172
				],
				[
					145.37743583739015,
					-1.1948799955352172
				],
				[
					146.9705889064725,
					-1.1948799955352172
				],
				[
					148.16548409573122,
					-1.1948799955352172
				],
				[
					149.7586675522605,
					-1.1948799955352172
				],
				[
					150.95353235407222,
					-1.1948799955352172
				],
				[
					152.5467158106015,
					-1.1948799955352172
				],
				[
					153.34332273258966,
					-1.1948799955352172
				],
				[
					154.93647580167195,
					-1.1948799955352172
				],
				[
					156.13137099093066,
					-1.1948799955352172
				],
				[
					156.52965925820124,
					-1.1948799955352172
				],
				[
					158.91941924927167,
					-1.1948799955352172
				],
				[
					160.11431443853039,
					-1.1948799955352172
				],
				[
					161.70749789505967,
					-1.1948799955352172
				],
				[
					162.90236269687145,
					-1.1948799955352172
				],
				[
					164.0972578861301,
					-1.1948799955352172
				],
				[
					165.6904413426594,
					-1.1948799955352172
				],
				[
					166.4870178772006,
					-1.1948799955352172
				],
				[
					166.88530614447117,
					-1.1948799955352172
				],
				[
					167.2836247991887,
					-1.1948799955352172
				],
				[
					168.08020133372983,
					-1.1948799955352172
				],
				[
					168.47848960100046,
					-1.1948799955352172
				],
				[
					169.27509652298855,
					-1.1948799955352172
				],
				[
					169.67338479025912,
					-1.1948799955352172
				],
				[
					170.46996132480032,
					-1.1948799955352172
				],
				[
					170.8682495920709,
					-1.1948799955352172
				],
				[
					171.2665682467884,
					-1.1948799955352172
				],
				[
					172.0631447813296,
					-1.1948799955352172
				],
				[
					172.46143304860018,
					-1.1948799955352172
				],
				[
					173.25803997058827,
					-1.1948799955352172
				],
				[
					173.6563282378589,
					-1.1948799955352172
				],
				[
					174.45290477240005,
					-1.1948799955352172
				],
				[
					174.85119303967062,
					-1.1948799955352172
				],
				[
					175.24951169438813,
					-1.1948799955352172
				],
				[
					176.04608822892934,
					-1.1948799955352172
				],
				[
					176.4443764961999,
					-1.1948799955352172
				],
				[
					177.24098341818805,
					-1.1948799955352172
				],
				[
					177.63927168545862,
					-1.1948799955352172
				],
				[
					178.0375599527292,
					-1.1948799955352172
				],
				[
					178.83413648727034,
					-1.1948799955352172
				],
				[
					179.2324551419879,
					-1.1948799955352172
				],
				[
					180.02903167652906,
					-1.1948799955352172
				],
				[
					180.42731994379963,
					-1.1948799955352172
				],
				[
					181.62221513305835,
					-1.1948799955352172
				],
				[
					182.02050340032892,
					-1.1948799955352172
				],
				[
					182.81707993487007,
					-1.1948799955352172
				],
				[
					184.01197512412878,
					-1.1948799955352172
				],
				[
					184.41026339139935,
					-1.1948799955352172
				],
				[
					185.2068703133875,
					-1.1948799955352172
				],
				[
					185.60515858065807,
					-1.1948799955352172
				],
				[
					186.00344684792864,
					-1.1948799955352172
				],
				[
					186.8000233824698,
					-1.1948799955352172
				],
				[
					187.19834203718736,
					-1.1948799955352172
				],
				[
					187.9949185717285,
					-1.1948799955352172
				],
				[
					188.39320683899908,
					-1.1948799955352172
				],
				[
					188.79149510626965,
					-1.1948799955352172
				],
				[
					189.5881020282578,
					-1.1948799955352172
				],
				[
					189.98639029552837,
					-1.1948799955352172
				],
				[
					190.78296683006957,
					-1.1948799955352172
				],
				[
					191.18128548478708,
					-1.1948799955352172
				],
				[
					191.97786201932823,
					-1.1948799955352172
				],
				[
					192.3761502865988,
					-1.1948799955352172
				],
				[
					192.77443855386943,
					-1.1948799955352172
				],
				[
					192.77443855386943,
					-1.1948799955352172
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 706,
			"versionNonce": 1240822579,
			"isDeleted": false,
			"id": "AthF6nqqqiTO6NrtGit0g",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -194.29961929332327,
			"y": -130.75318415305279,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 196.7574123889161,
			"height": 4.381231714870296,
			"seed": 440953128,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.7965917282646444
				],
				[
					0.39828826727057276,
					-0.7965917282646444
				],
				[
					0.7965765345411455,
					-0.7965917282646444
				],
				[
					1.9914717237998616,
					-0.7965917282646444
				],
				[
					3.1863365256116083,
					-0.7965917282646444
				],
				[
					4.381231714870324,
					-0.7965917282646444
				],
				[
					5.576126904128984,
					-0.7965917282646444
				],
				[
					6.770991705940759,
					-0.7965917282646444
				],
				[
					9.160751697011193,
					-0.7965917282646444
				],
				[
					12.745406877340343,
					-0.7965917282646444
				],
				[
					17.52495724692821,
					-0.7965917282646444
				],
				[
					21.10958203981042,
					-0.7965917282646444
				],
				[
					25.88913240939823,
					-0.7965917282646444
				],
				[
					31.46525931352724,
					-0.7965917282646444
				],
				[
					37.04135583020931,
					-0.7965917282646444
				],
				[
					43.41408965632647,
					-0.7965917282646444
				],
				[
					48.99018617300854,
					-0.7965917282646444
				],
				[
					54.56631307713755,
					-0.7965917282646444
				],
				[
					60.14243998126656,
					-1.59316826280579
				],
				[
					67.71003860919544,
					-1.59316826280579
				],
				[
					72.4895585913363,
					-1.59316826280579
				],
				[
					76.87079030620666,
					-1.59316826280579
				],
				[
					80.85373375380638,
					-1.59316826280579
				],
				[
					84.04010066686496,
					-1.59316826280579
				],
				[
					86.03157239066482,
					-1.59316826280579
				],
				[
					88.02304411446468,
					-1.59316826280579
				],
				[
					88.81962064900583,
					-1.59316826280579
				],
				[
					90.01451583826454,
					-1.59316826280579
				],
				[
					91.2094110275232,
					-1.59316826280579
				],
				[
					92.40427582933498,
					-1.59316826280579
				],
				[
					92.80256409660555,
					-1.59316826280579
				],
				[
					93.99745928586427,
					-1.59316826280579
				],
				[
					95.19235447512298,
					-1.59316826280579
				],
				[
					96.78550754420527,
					-1.59316826280579
				],
				[
					98.77697926800514,
					-1.59316826280579
				],
				[
					100.37016272453442,
					-1.59316826280579
				],
				[
					103.556529637593,
					-1.59316826280579
				],
				[
					107.14118481792215,
					-1.59316826280579
				],
				[
					111.12412826552188,
					-1.1948799955352172
				],
				[
					115.1070717131216,
					-1.1948799955352172
				],
				[
					118.69169650600381,
					-1.1948799955352172
				],
				[
					122.67463995360353,
					-0.39828826727057276
				],
				[
					126.65758340120325,
					-0.39828826727057276
				],
				[
					130.2422385815324,
					-0.39828826727057276
				],
				[
					133.42860549459098,
					-0.39828826727057276
				],
				[
					135.81836548566142,
					-0.39828826727057276
				],
				[
					138.60641374400248,
					-0.39828826727057276
				],
				[
					140.99620412251986,
					-0.39828826727057276
				],
				[
					143.3859641135903,
					-0.39828826727057276
				],
				[
					144.58082891540207,
					0
				],
				[
					145.3774358373902,
					0
				],
				[
					145.77572410466078,
					0
				],
				[
					146.17401237193135,
					0
				],
				[
					146.97061929391944,
					0
				],
				[
					147.36890756119007,
					0
				],
				[
					148.16548409573122,
					0
				],
				[
					148.96209101771936,
					0
				],
				[
					150.95356274151922,
					0
				],
				[
					152.14842754333094,
					0.39830346099407166
				],
				[
					154.1398992671308,
					0.39830346099407166
				],
				[
					156.13137099093066,
					1.1948799955352456
				],
				[
					158.5211309820011,
					1.1948799955352456
				],
				[
					160.51260270580102,
					1.5931834565292888
				],
				[
					162.9023930843184,
					1.5931834565292888
				],
				[
					165.29215307538882,
					1.5931834565292888
				],
				[
					167.68191306645926,
					2.3897751847939332
				],
				[
					169.27509652298855,
					2.3897751847939332
				],
				[
					171.2665682467884,
					2.3897751847939332
				],
				[
					172.8597517033177,
					2.3897751847939332
				],
				[
					175.2495116943882,
					2.3897751847939332
				],
				[
					175.64779996165876,
					2.3897751847939332
				],
				[
					176.4443764961999,
					2.3897751847939332
				],
				[
					177.24098341818805,
					2.3897751847939332
				],
				[
					178.0375599527292,
					2.3897751847939332
				],
				[
					178.43584821999977,
					2.3897751847939332
				],
				[
					179.2324551419879,
					2.3897751847939332
				],
				[
					179.63074340925849,
					2.3897751847939332
				],
				[
					180.42731994379963,
					2.3897751847939332
				],
				[
					180.8256385985172,
					2.3897751847939332
				],
				[
					181.22392686578777,
					2.788063452064506
				],
				[
					182.02050340032892,
					2.788063452064506
				],
				[
					182.4187916675995,
					2.788063452064506
				],
				[
					183.21539858958764,
					2.788063452064506
				],
				[
					183.6136868568582,
					2.788063452064506
				],
				[
					184.01197512412878,
					2.788063452064506
				],
				[
					184.80858204611692,
					2.788063452064506
				],
				[
					185.2068703133875,
					2.788063452064506
				],
				[
					186.00344684792864,
					2.788063452064506
				],
				[
					186.40173511519922,
					2.788063452064506
				],
				[
					187.19834203718736,
					2.788063452064506
				],
				[
					187.59663030445793,
					2.788063452064506
				],
				[
					187.9949185717285,
					2.788063452064506
				],
				[
					188.79152549371665,
					2.788063452064506
				],
				[
					189.18981376098722,
					2.788063452064506
				],
				[
					189.98639029552837,
					2.788063452064506
				],
				[
					190.384678562799,
					2.788063452064506
				],
				[
					191.18128548478708,
					2.788063452064506
				],
				[
					191.97786201932823,
					2.788063452064506
				],
				[
					192.77446894131637,
					2.788063452064506
				],
				[
					193.17275720858694,
					2.788063452064506
				],
				[
					194.36762201039872,
					2.788063452064506
				],
				[
					194.76594066511623,
					2.788063452064506
				],
				[
					195.56251719965738,
					2.788063452064506
				],
				[
					195.960805466928,
					2.788063452064506
				],
				[
					196.7574123889161,
					2.788063452064506
				],
				[
					196.7574123889161,
					2.788063452064506
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 626,
			"versionNonce": 280284541,
			"isDeleted": false,
			"id": "5GqsIW0a",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -120.28388644477747,
			"y": 72.47651133821293,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 31.775985717773438,
			"height": 20,
			"seed": 1206487128,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "main",
			"rawText": "main",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "main",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 619,
			"versionNonce": 468096211,
			"isDeleted": false,
			"id": "UHNNEySd",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -136.52480956369186,
			"y": 39.01981068833268,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 63.50395202636719,
			"height": 20,
			"seed": 831641896,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "print1 (1)",
			"rawText": "print1 (1)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print1 (1)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 706,
			"versionNonce": 1796740573,
			"isDeleted": false,
			"id": "pGiX8u76",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -157.8919681586288,
			"y": 1.8362034259963878,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 77.61595153808594,
			"height": 20,
			"seed": 543931688,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "print2 (2)",
			"rawText": "print2 (2)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print2 (2)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 728,
			"versionNonce": 42107507,
			"isDeleted": false,
			"id": "UHSlshny",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -157.2240530219418,
			"y": -79.21670484889222,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 75.31193542480469,
			"height": 20,
			"seed": 350498136,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "print4 (4)",
			"rawText": "print4 (4)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print4 (4)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 695,
			"versionNonce": 1051939389,
			"isDeleted": false,
			"id": "rJQESOa5",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -157.3996974287317,
			"y": -35.90217966252166,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 76.62394714355469,
			"height": 20,
			"seed": 417991768,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "print3 (3)",
			"rawText": "print3 (3)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print3 (3)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 699,
			"versionNonce": 915389459,
			"isDeleted": false,
			"id": "sIkju25D",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -153.08122037046724,
			"y": -118.34912726030427,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 74.60792541503906,
			"height": 20,
			"seed": 1788705880,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "print5 (5)",
			"rawText": "print5 (5)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print5 (5)",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 609,
			"versionNonce": 141034141,
			"isDeleted": false,
			"id": "lYS4Z60wUFUwjKWxUKOz7",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -154.2930620711977,
			"y": -96.36318044485961,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 89.0585875813847,
			"height": 16.070729101050404,
			"seed": 289179176,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.3392061386545038,
					0
				],
				[
					2.0088602954211865,
					0
				],
				[
					4.017669503402772,
					0
				],
				[
					6.026529798823844,
					0
				],
				[
					8.704993163572226,
					-0.669603069327195
				],
				[
					10.713802371553811,
					-0.669603069327195
				],
				[
					13.392265736302079,
					-2.008834751701329
				],
				[
					16.740332170377656,
					-2.6784633647483247
				],
				[
					20.08839860445312,
					-4.017669503402715
				],
				[
					24.10606810785589,
					-4.687298116449654
				],
				[
					30.80220097600693,
					-6.6961328681510395
				],
				[
					39.50719413957904,
					-9.374596232899364
				],
				[
					44.8640697816362,
					-10.04419930222656
				],
				[
					51.56020264978724,
					-12.053034053927888
				],
				[
					57.58673244861109,
					-12.053034053927888
				],
				[
					64.28286531676213,
					-13.392265736302079
				],
				[
					69.63979204625878,
					-14.731497418676213
				],
				[
					74.32706461898874,
					-14.731497418676213
				],
				[
					78.3447341223914,
					-14.731497418676213
				],
				[
					80.35359441781247,
					-14.731497418676213
				],
				[
					82.36245471323366,
					-15.401100488003408
				],
				[
					83.03205778256086,
					-15.401100488003408
				],
				[
					84.37126392121525,
					-16.070729101050404
				],
				[
					85.04086699054244,
					-16.070729101050404
				],
				[
					86.38012421663632,
					-16.070729101050404
				],
				[
					87.04972728596351,
					-16.070729101050404
				],
				[
					88.38893342461802,
					-16.070729101050404
				],
				[
					89.0585875813847,
					-16.070729101050404
				],
				[
					89.0585875813847,
					-16.070729101050404
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 605,
			"versionNonce": 335856051,
			"isDeleted": false,
			"id": "qXd0NsH0G72X-tHk2HhFo",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -143.5792596996439,
			"y": -61.54328442173022,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 89.0585364939451,
			"height": 9.37457068917962,
			"seed": 1050512168,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.33920613865439,
					0
				],
				[
					-2.008809207981585,
					0
				],
				[
					-0.669603069327195,
					0
				],
				[
					1.3392572260938778,
					0
				],
				[
					4.017669503402772,
					0.669603069327195
				],
				[
					6.6961328681510395,
					0.669603069327195
				],
				[
					10.713802371553811,
					0.669603069327195
				],
				[
					14.731522962395957,
					0.669603069327195
				],
				[
					22.09725889987419,
					0.669603069327195
				],
				[
					28.79339176802523,
					0
				],
				[
					35.48952463617627,
					-0.6696286130469957
				],
				[
					42.18565750432731,
					-2.008834751701386
				],
				[
					48.212187303151154,
					-3.3480664340755197
				],
				[
					54.908320171302194,
					-4.6872981164497105
				],
				[
					61.60445303945323,
					-4.6872981164497105
				],
				[
					66.9613286815104,
					-6.6961328681510395
				],
				[
					72.31825541100704,
					-6.6961328681510395
				],
				[
					77.00552798373701,
					-7.365761481198035
				],
				[
					81.02319748713967,
					-7.365761481198035
				],
				[
					83.03205778256074,
					-8.704967619852425
				],
				[
					84.37126392121525,
					-8.704967619852425
				],
				[
					85.04091807798193,
					-8.704967619852425
				],
				[
					85.71052114730912,
					-8.704967619852425
				],
				[
					87.04972728596351,
					-8.704967619852425
				],
				[
					87.04972728596351,
					-8.704967619852425
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 618,
			"versionNonce": 753379069,
			"isDeleted": false,
			"id": "4qP4pOIwG1js-OqYVqpfx",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -153.6234590018704,
			"y": -15.339957414000196,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 103.12045638701386,
			"height": 12.053008510208201,
			"seed": 1585349672,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					4.687323660169341,
					1.339206138654447
				],
				[
					5.356926729496536,
					1.339206138654447
				],
				[
					7.3657359374782345,
					1.339206138654447
				],
				[
					10.044199302226502,
					1.339206138654447
				],
				[
					14.061868805629274,
					0.6696030693272519
				],
				[
					18.07958939647142,
					0
				],
				[
					26.11492840327685,
					-1.3392572260938778
				],
				[
					34.15026741008239,
					-2.678463364748268
				],
				[
					40.84640027823343,
					-3.3480664340755197
				],
				[
					48.88179037247835,
					-4.6873236601693975
				],
				[
					53.569062945208316,
					-4.6873236601693975
				],
				[
					60.265195813359355,
					-6.026529798823788
				],
				[
					65.62212254285589,
					-6.6961328681510395
				],
				[
					69.63979204625866,
					-6.6961328681510395
				],
				[
					72.98785848033413,
					-6.6961328681510395
				],
				[
					76.3359249144097,
					-6.6961328681510395
				],
				[
					79.01438827915797,
					-6.6961328681510395
				],
				[
					79.68399134848516,
					-6.6961328681510395
				],
				[
					81.69285164390635,
					-6.6961328681510395
				],
				[
					83.70166085188794,
					-6.6961328681510395
				],
				[
					85.71052114730901,
					-6.6961328681510395
				],
				[
					86.3801242166362,
					-6.6961328681510395
				],
				[
					88.38898451205739,
					-8.035390094244917
				],
				[
					89.72819065071178,
					-8.035390094244917
				],
				[
					90.39779372003898,
					-8.035390094244917
				],
				[
					91.73705094613285,
					-8.035390094244917
				],
				[
					92.40665401546005,
					-8.035390094244917
				],
				[
					93.07625708478724,
					-8.704993163572112
				],
				[
					95.08511738020843,
					-8.704993163572112
				],
				[
					96.42432351886282,
					-8.704993163572112
				],
				[
					97.09392658819002,
					-8.704993163572112
				],
				[
					97.76352965751721,
					-10.04419930222656
				],
				[
					99.10278688361109,
					-10.04419930222656
				],
				[
					99.77238995293828,
					-10.713802371553754
				],
				[
					101.11159609159279,
					-10.713802371553754
				],
				[
					101.78125024835947,
					-10.713802371553754
				],
				[
					103.12045638701386,
					-10.713802371553754
				],
				[
					103.12045638701386,
					-10.713802371553754
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 605,
			"versionNonce": 872944467,
			"isDeleted": false,
			"id": "xN56fwjMeH1pszRXM7XfV",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -140.90079633489563,
			"y": 12.783780197258409,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 86.38012421663632,
			"height": 10.713802371553754,
			"seed": 471284776,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.6696030693273087,
					0
				],
				[
					2.0088602954211865,
					0.669603069327195
				],
				[
					4.017669503402772,
					0.669603069327195
				],
				[
					5.356926729496649,
					2.008860295421073
				],
				[
					7.365735937478348,
					2.008860295421073
				],
				[
					10.044199302226616,
					2.008860295421073
				],
				[
					13.392265736302079,
					2.008860295421073
				],
				[
					17.40993523970485,
					2.008860295421073
				],
				[
					23.436465038528695,
					1.3392572260938778
				],
				[
					30.132597906679734,
					0
				],
				[
					38.167936913485164,
					-1.339206138654447
				],
				[
					46.872930077057276,
					-3.3480664340755197
				],
				[
					54.90826908386282,
					-4.687272572729967
				],
				[
					62.94365917810774,
					-6.026529798823844
				],
				[
					69.63979204625878,
					-6.026529798823844
				],
				[
					74.99666768831594,
					-6.6961328681510395
				],
				[
					79.01438827915808,
					-6.6961328681510395
				],
				[
					80.35359441781247,
					-6.6961328681510395
				],
				[
					81.69280055646698,
					-8.035339006805486
				],
				[
					82.36245471323366,
					-8.035339006805486
				],
				[
					83.70166085188805,
					-8.704942076132681
				],
				[
					84.37126392121525,
					-8.704942076132681
				],
				[
					85.71052114730912,
					-8.704942076132681
				],
				[
					86.38012421663632,
					-8.704942076132681
				],
				[
					86.38012421663632,
					-8.704942076132681
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 600,
			"versionNonce": 2125709149,
			"isDeleted": false,
			"id": "9nfJHOw7d_bxmINxnc_AD",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -142.9096566303167,
			"y": 52.960577406164646,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 103.79005945634117,
			"height": 2.008809207981642,
			"seed": 407295272,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					3.3480664340755766,
					0
				],
				[
					5.356926729496649,
					0
				],
				[
					9.374596232899421,
					0
				],
				[
					13.392265736302079,
					0
				],
				[
					19.418795535125923,
					0
				],
				[
					27.45418562937084,
					0
				],
				[
					35.48952463617627,
					0
				],
				[
					43.52486364298181,
					-0.6696030693272519
				],
				[
					52.89945987588112,
					-0.6696030693272519
				],
				[
					62.27405610878043,
					-2.008809207981642
				],
				[
					72.98785848033424,
					-2.008809207981642
				],
				[
					82.36245471323355,
					-2.008809207981642
				],
				[
					89.7281906507119,
					-2.008809207981642
				],
				[
					95.08511738020843,
					-2.008809207981642
				],
				[
					99.1027868836112,
					-2.008809207981642
				],
				[
					101.11164717903227,
					-2.008809207981642
				],
				[
					101.78125024835947,
					-2.008809207981642
				],
				[
					103.12045638701397,
					-2.008809207981642
				],
				[
					103.79005945634117,
					-2.008809207981642
				],
				[
					103.79005945634117,
					-2.008809207981642
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 601,
			"versionNonce": 1190146291,
			"isDeleted": false,
			"id": "qOFAv82seqHN0Nc9C-O2f",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -126.83892752926624,
			"y": 91.79816847641644,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 46.20332700772997,
			"height": 8.035390094244917,
			"seed": 785876776,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					4.687323660169341,
					0
				],
				[
					6.6961328681510395,
					0
				],
				[
					10.044199302226502,
					0
				],
				[
					14.061868805629274,
					-1.3392572260938778
				],
				[
					16.740332170377542,
					-1.3392572260938778
				],
				[
					20.758001673780313,
					-2.008860295421073
				],
				[
					23.43646503852858,
					-3.3480664340755197
				],
				[
					27.454134541931353,
					-4.017669503402715
				],
				[
					30.13259790667962,
					-4.017669503402715
				],
				[
					32.81106127142789,
					-5.3569267294965925
				],
				[
					36.159127705503465,
					-6.026529798823844
				],
				[
					37.498333844157855,
					-6.026529798823844
				],
				[
					39.50719413957893,
					-7.3657359374782345
				],
				[
					40.84640027823343,
					-8.035390094244917
				],
				[
					41.516054435000115,
					-8.035390094244917
				],
				[
					42.855260573654505,
					-8.035390094244917
				],
				[
					43.5248636429817,
					-8.035390094244917
				],
				[
					44.194466712308895,
					-8.035390094244917
				],
				[
					45.53372393840277,
					-8.035390094244917
				],
				[
					46.20332700772997,
					-8.035390094244917
				],
				[
					46.20332700772997,
					-8.035390094244917
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 694,
			"versionNonce": 69061565,
			"isDeleted": false,
			"id": "zv91GZkYWUSXk71ed1pPY",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 21.815201708711015,
			"y": -143.23611052191688,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 7.365787024917722,
			"height": 237.04308820631496,
			"seed": 238375976,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.669603069327195
				],
				[
					0,
					2.6784633647483247
				],
				[
					0,
					3.3480664340755197
				],
				[
					0,
					5.3569011857769055
				],
				[
					0,
					7.3657359374782345
				],
				[
					0,
					10.04419930222656
				],
				[
					0,
					12.053034053927945
				],
				[
					0,
					14.73149741867627
				],
				[
					0,
					17.409935239704794
				],
				[
					0,
					20.758001673780313
				],
				[
					0,
					22.766861969201443
				],
				[
					-0.6695519818877074,
					25.445299790230024
				],
				[
					-2.008758120542211,
					28.12376315497835
				],
				[
					-2.008758120542211,
					30.802200976006873
				],
				[
					-2.008758120542211,
					32.811061271428
				],
				[
					-2.008758120542211,
					35.48949909245658
				],
				[
					-2.008758120542211,
					37.49833384415791
				],
				[
					-2.008758120542211,
					38.8375655265321
				],
				[
					-2.008758120542211,
					40.84640027823343
				],
				[
					-2.008758120542211,
					42.18563196060762
				],
				[
					-2.008758120542211,
					44.19446671230895
				],
				[
					-2.008758120542211,
					45.53369839468314
				],
				[
					-2.008758120542211,
					46.20332700773008
				],
				[
					-2.678412277308894,
					47.54253314638447
				],
				[
					-2.678412277308894,
					48.21216175943147
				],
				[
					-2.678412277308894,
					50.220996511132796
				],
				[
					-2.678412277308894,
					50.89059958045999
				],
				[
					-2.678412277308894,
					53.569062945208316
				],
				[
					-2.678412277308894,
					55.5778976969097
				],
				[
					-2.678412277308894,
					58.92596413098522
				],
				[
					-4.017618415963284,
					61.604427495733546
				],
				[
					-4.017618415963284,
					65.62209699913626
				],
				[
					-4.017618415963284,
					66.9613286815104
				],
				[
					-4.017618415963284,
					70.30939511558591
				],
				[
					-4.017618415963284,
					71.6486267979601
				],
				[
					-4.687272572729967,
					74.99669323203562
				],
				[
					-4.687272572729967,
					77.67513105306415
				],
				[
					-5.356824554617674,
					80.35359441781247
				],
				[
					-5.356824554617674,
					84.37126392121519
				],
				[
					-5.356824554617674,
					87.04972728596351
				],
				[
					-5.356824554617674,
					90.39779372003903
				],
				[
					-5.356824554617674,
					93.07623154106761
				],
				[
					-6.6961328681510395,
					97.09395213190982
				],
				[
					-6.6961328681510395,
					99.77236440921865
				],
				[
					-6.6961328681510395,
					101.78122470463978
				],
				[
					-6.6961328681510395,
					103.79008500006086
				],
				[
					-6.6961328681510395,
					105.7988942080425
				],
				[
					-6.6961328681510395,
					106.46849727736969
				],
				[
					-6.6961328681510395,
					108.47735757279082
				],
				[
					-6.6961328681510395,
					110.4862178682119
				],
				[
					-6.6961328681510395,
					111.15582093753909
				],
				[
					-6.6961328681510395,
					113.16463014552073
				],
				[
					-6.6961328681510395,
					115.17349044094186
				],
				[
					-6.6961328681510395,
					117.18235073636293
				],
				[
					-6.6961328681510395,
					119.19115994434458
				],
				[
					-6.6961328681510395,
					120.53041717043845
				],
				[
					-6.6961328681510395,
					122.5392263784201
				],
				[
					-6.6961328681510395,
					125.21768974316842
				],
				[
					-6.6961328681510395,
					128.56575617724394
				],
				[
					-6.6961328681510395,
					130.574616472665
				],
				[
					-6.6961328681510395,
					133.25302874997385
				],
				[
					-6.6961328681510395,
					135.93149211472218
				],
				[
					-6.6961328681510395,
					137.94035241014325
				],
				[
					-6.6961328681510395,
					140.61881577489157
				],
				[
					-6.6961328681510395,
					143.9668822089671
				],
				[
					-6.6961328681510395,
					146.64529448627593
				],
				[
					-6.6961328681510395,
					149.32375785102425
				],
				[
					-6.6961328681510395,
					154.68068458052085
				],
				[
					-6.6961328681510395,
					158.69835408392356
				],
				[
					-6.026478711384357,
					162.71602358732633
				],
				[
					-6.026478711384357,
					165.3944869520746
				],
				[
					-5.356824554617674,
					169.41215645547737
				],
				[
					-5.356824554617674,
					172.09061982022564
				],
				[
					-5.356824554617674,
					174.76908318497397
				],
				[
					-5.356824554617674,
					176.7778923929556
				],
				[
					-4.017618415963284,
					178.78675268837668
				],
				[
					-4.017618415963284,
					180.7956129837978
				],
				[
					-4.017618415963284,
					182.80442219177945
				],
				[
					-4.017618415963284,
					184.81328248720052
				],
				[
					-4.017618415963284,
					185.48288555652772
				],
				[
					-4.017618415963284,
					186.15248862585497
				],
				[
					-4.017618415963284,
					187.49174585194885
				],
				[
					-4.017618415963284,
					188.16134892127604
				],
				[
					-4.017618415963284,
					189.5005550599305
				],
				[
					-4.017618415963284,
					190.1701581292577
				],
				[
					-4.017618415963284,
					190.83981228602437
				],
				[
					-4.017618415963284,
					192.848621494006
				],
				[
					-3.3480664340755766,
					194.85748178942708
				],
				[
					-3.3480664340755766,
					196.86629099740873
				],
				[
					-3.3480664340755766,
					198.8751512928298
				],
				[
					-3.3480664340755766,
					200.88401158825093
				],
				[
					-2.008758120542211,
					203.56242386555977
				],
				[
					-2.008758120542211,
					205.57128416098084
				],
				[
					-2.008758120542211,
					208.24974752572916
				],
				[
					-1.33920613865439,
					210.2585567337108
				],
				[
					-1.33920613865439,
					212.93702009845913
				],
				[
					-1.33920613865439,
					214.9458803938802
				],
				[
					-0.6695519818877074,
					217.62434375862853
				],
				[
					-0.6695519818877074,
					219.63315296661017
				],
				[
					-0.6695519818877074,
					222.31161633135844
				],
				[
					-0.6695519818877074,
					224.32047662677957
				],
				[
					0.6696541567666827,
					226.3292858347612
				],
				[
					0.6696541567666827,
					228.33814613018228
				],
				[
					0.6696541567666827,
					230.34695533816392
				],
				[
					0.6696541567666827,
					232.355815633585
				],
				[
					0.6696541567666827,
					233.02541870291225
				],
				[
					0.6696541567666827,
					233.69502177223944
				],
				[
					0.6696541567666827,
					235.03427899833332
				],
				[
					0.6696541567666827,
					235.70388206766052
				],
				[
					0.6696541567666827,
					237.04308820631496
				],
				[
					0,
					237.04308820631496
				],
				[
					-0.6695519818877074,
					237.04308820631496
				],
				[
					-1.33920613865439,
					236.37348513698777
				],
				[
					-1.33920613865439,
					236.37348513698777
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 611,
			"versionNonce": 776182419,
			"isDeleted": false,
			"id": "tHtBcVVupWPnNCkHPefSF",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 14.449516858672268,
			"y": 81.08436610486268,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 22.09725889987419,
			"height": 15.401074944283721,
			"seed": 2053427240,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.33920613865439,
					0
				],
				[
					2.008860295421073,
					0
				],
				[
					3.348066434075463,
					0
				],
				[
					3.348066434075463,
					1.33920613865439
				],
				[
					4.01761841596317,
					2.008809207981642
				],
				[
					4.01761841596317,
					3.3480664340755197
				],
				[
					5.356926729496536,
					4.68727257272991
				],
				[
					5.356926729496536,
					6.026478711384357
				],
				[
					5.356926729496536,
					6.6961328681510395
				],
				[
					6.026478711384357,
					8.704942076132681
				],
				[
					6.6961328681510395,
					10.713802371553754
				],
				[
					6.6961328681510395,
					12.722611579535396
				],
				[
					8.03533900680543,
					13.392265736302079
				],
				[
					8.03533900680543,
					14.731471874956469
				],
				[
					8.03533900680543,
					15.401074944283721
				],
				[
					8.704993163572112,
					15.401074944283721
				],
				[
					10.044199302226502,
					15.401074944283721
				],
				[
					10.71375128411421,
					15.401074944283721
				],
				[
					12.053059597647575,
					15.401074944283721
				],
				[
					14.731471874956469,
					11.38340544088095
				],
				[
					15.401126031723152,
					9.374545145459876
				],
				[
					17.40988415226525,
					7.3657359374782345
				],
				[
					18.749192465798615,
					5.356875642057162
				],
				[
					20.08839860445312,
					3.3480664340755197
				],
				[
					20.08839860445312,
					2.678412277308837
				],
				[
					21.42760474310751,
					2.678412277308837
				],
				[
					21.42760474310751,
					1.33920613865439
				],
				[
					22.09725889987419,
					0.669603069327195
				],
				[
					22.09725889987419,
					2.008809207981642
				],
				[
					22.09725889987419,
					2.678412277308837
				],
				[
					22.09725889987419,
					2.678412277308837
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 804,
			"versionNonce": 2101824541,
			"isDeleted": false,
			"id": "UJaDSCff",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 1.5944815347316315,
			"x": -102.22123904517116,
			"y": -48.82064729847514,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 224.8638458251953,
			"height": 20,
			"seed": 1898572584,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "order of removal from stack",
			"rawText": "order of removal from stack",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "order of removal from stack",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 664,
			"versionNonce": 1454952499,
			"isDeleted": false,
			"id": "yueVu3zvU3MMW3OpwQIn_",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -220.5847876833808,
			"y": 100.5031616399886,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 12.722662666974884,
			"height": 231.6862125642578,
			"seed": 2146212904,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-1.3392572260938778
				],
				[
					0,
					-2.008860295421073
				],
				[
					0,
					-2.678463364748268
				],
				[
					0,
					-4.017720590842259
				],
				[
					0,
					-4.687323660169454
				],
				[
					0,
					-6.026529798823844
				],
				[
					0,
					-6.6961328681510395
				],
				[
					0,
					-7.365787024917722
				],
				[
					0.669603069327195,
					-8.70499316357217
				],
				[
					0.669603069327195,
					-9.374596232899364
				],
				[
					1.3392572260938778,
					-10.713853458993242
				],
				[
					1.3392572260938778,
					-12.722662666974884
				],
				[
					2.678463364748268,
					-14.061919893068762
				],
				[
					2.678463364748268,
					-15.401126031723209
				],
				[
					2.678463364748268,
					-16.070729101050404
				],
				[
					2.678463364748268,
					-18.079589396471476
				],
				[
					3.348066434075463,
					-19.418795535125923
				],
				[
					3.348066434075463,
					-20.08839860445312
				],
				[
					3.348066434075463,
					-22.097258899874248
				],
				[
					3.348066434075463,
					-24.10611919529532
				],
				[
					3.348066434075463,
					-26.784531472604158
				],
				[
					3.348066434075463,
					-28.793391768025288
				],
				[
					3.348066434075463,
					-30.80225206344636
				],
				[
					3.348066434075463,
					-32.14145820210081
				],
				[
					3.348066434075463,
					-33.4806643407552
				],
				[
					3.348066434075463,
					-35.48952463617633
				],
				[
					3.348066434075463,
					-37.4983849315974
				],
				[
					3.348066434075463,
					-38.167988000924595
				],
				[
					3.348066434075463,
					-40.17679720890624
				],
				[
					3.348066434075463,
					-42.18565750432737
				],
				[
					3.348066434075463,
					-42.85526057365456
				],
				[
					3.348066434075463,
					-44.864120869075634
				],
				[
					3.348066434075463,
					-45.533723938402886
				],
				[
					3.348066434075463,
					-46.872930077057276
				],
				[
					3.348066434075463,
					-48.881790372478406
				],
				[
					3.348066434075463,
					-50.220996511132796
				],
				[
					3.348066434075463,
					-51.560253737226674
				],
				[
					3.348066434075463,
					-52.229856806553926
				],
				[
					3.348066434075463,
					-53.569062945208316
				],
				[
					3.348066434075463,
					-55.577923240629445
				],
				[
					3.348066434075463,
					-56.917129379283836
				],
				[
					3.348066434075463,
					-58.925989674704965
				],
				[
					3.348066434075463,
					-60.265195813359355
				],
				[
					3.348066434075463,
					-62.274056108780485
				],
				[
					2.008860295421073,
					-63.613262247434875
				],
				[
					2.008860295421073,
					-65.622122542856
				],
				[
					1.3392572260938778,
					-67.63098283827708
				],
				[
					0.669603069327195,
					-69.63979204625872
				],
				[
					0.669603069327195,
					-71.64865234167979
				],
				[
					-0.6696030693273087,
					-73.65746154966143
				],
				[
					-1.3392061386545038,
					-74.99671877575531
				],
				[
					-1.3392061386545038,
					-77.00552798373695
				],
				[
					-1.3392061386545038,
					-78.34478520983083
				],
				[
					-1.3392061386545038,
					-81.02324857457916
				],
				[
					-1.3392061386545038,
					-81.69285164390635
				],
				[
					-1.3392061386545038,
					-83.701660851888
				],
				[
					-1.3392061386545038,
					-85.71052114730912
				],
				[
					-1.3392061386545038,
					-87.7193814427302
				],
				[
					-1.3392061386545038,
					-89.72819065071184
				],
				[
					-1.3392061386545038,
					-91.73705094613291
				],
				[
					-1.3392061386545038,
					-93.07625708478736
				],
				[
					-1.3392061386545038,
					-95.08511738020843
				],
				[
					0,
					-97.09392658819007
				],
				[
					0,
					-99.10278688361115
				],
				[
					0,
					-101.11164717903227
				],
				[
					0,
					-101.78125024835947
				],
				[
					0,
					-103.12045638701392
				],
				[
					0,
					-103.79005945634111
				],
				[
					0,
					-105.79891975176218
				],
				[
					0,
					-106.46852282108944
				],
				[
					0,
					-108.47738311651051
				],
				[
					0,
					-109.81658925516496
				],
				[
					0.669603069327195,
					-111.82544955058603
				],
				[
					0.669603069327195,
					-112.49505261991322
				],
				[
					0.669603069327195,
					-114.50391291533435
				],
				[
					0.669603069327195,
					-115.17351598466155
				],
				[
					1.3392572260938778,
					-117.18232519264319
				],
				[
					1.3392572260938778,
					-117.85197934940987
				],
				[
					1.3392572260938778,
					-119.86078855739152
				],
				[
					1.3392572260938778,
					-121.86964885281259
				],
				[
					1.3392572260938778,
					-123.87845806079423
				],
				[
					1.3392572260938778,
					-126.55692142554255
				],
				[
					1.3392572260938778,
					-129.90498785961807
				],
				[
					1.3392572260938778,
					-131.24424508571195
				],
				[
					1.3392572260938778,
					-134.59231151978747
				],
				[
					1.3392572260938778,
					-135.93151765844186
				],
				[
					1.3392572260938778,
					-139.27958409251738
				],
				[
					1.3392572260938778,
					-141.9580474572657
				],
				[
					1.3392572260938778,
					-145.97571696066842
				],
				[
					1.3392572260938778,
					-148.65418032541675
				],
				[
					1.3392572260938778,
					-152.67184982881946
				],
				[
					1.3392572260938778,
					-155.35031319356779
				],
				[
					1.3392572260938778,
					-158.02875101459637
				],
				[
					1.3392572260938778,
					-161.3768174486719
				],
				[
					1.3392572260938778,
					-164.0552808134202
				],
				[
					1.3392572260938778,
					-166.06411556512154
				],
				[
					1.3392572260938778,
					-168.74257892986986
				],
				[
					1.3392572260938778,
					-171.42101675089845
				],
				[
					1.3392572260938778,
					-173.42987704631958
				],
				[
					1.3392572260938778,
					-175.4387117980209
				],
				[
					1.3392572260938778,
					-178.11714961904948
				],
				[
					1.3392572260938778,
					-180.12600991447061
				],
				[
					1.3392572260938778,
					-182.13484466617194
				],
				[
					2.678463364748268,
					-182.80444773549914
				],
				[
					2.678463364748268,
					-184.81328248720052
				],
				[
					3.348066434075463,
					-186.15251416957466
				],
				[
					3.348066434075463,
					-186.82214278262165
				],
				[
					3.348066434075463,
					-187.49174585194885
				],
				[
					3.348066434075463,
					-188.83097753432298
				],
				[
					4.687323660169341,
					-189.50058060365018
				],
				[
					4.687323660169341,
					-190.83981228602437
				],
				[
					4.687323660169341,
					-191.50941535535156
				],
				[
					5.356926729496536,
					-191.50941535535156
				],
				[
					5.356926729496536,
					-192.8486470377257
				],
				[
					5.356926729496536,
					-193.5182756507727
				],
				[
					6.026529798823731,
					-193.5182756507727
				],
				[
					6.026529798823731,
					-194.1878787200999
				],
				[
					6.026529798823731,
					-195.52711040247402
				],
				[
					6.026529798823731,
					-196.19671347180122
				],
				[
					6.026529798823731,
					-197.5359451541754
				],
				[
					6.026529798823731,
					-198.2055482235026
				],
				[
					6.026529798823731,
					-199.54477990587674
				],
				[
					6.026529798823731,
					-200.21440851892373
				],
				[
					6.026529798823731,
					-202.22324327062506
				],
				[
					6.026529798823731,
					-204.23207802232645
				],
				[
					6.026529798823731,
					-205.57130970470058
				],
				[
					6.026529798823731,
					-207.58014445640197
				],
				[
					6.026529798823731,
					-209.5889792081033
				],
				[
					6.026529798823731,
					-210.9282108904775
				],
				[
					7.3657359374782345,
					-213.6066742552258
				],
				[
					7.3657359374782345,
					-215.61550900692714
				],
				[
					7.3657359374782345,
					-216.28511207625434
				],
				[
					8.035390094244917,
					-218.29394682795572
				],
				[
					8.035390094244917,
					-218.96357544100266
				],
				[
					8.035390094244917,
					-220.30280712337685
				],
				[
					9.374596232899307,
					-220.97241019270405
				],
				[
					9.374596232899307,
					-222.98124494440538
				],
				[
					9.374596232899307,
					-224.32047662677957
				],
				[
					10.044199302226502,
					-224.99007969610676
				],
				[
					10.044199302226502,
					-226.9989399915279
				],
				[
					10.044199302226502,
					-227.6685430608551
				],
				[
					10.044199302226502,
					-229.00777474322922
				],
				[
					10.044199302226502,
					-229.67737781255641
				],
				[
					10.044199302226502,
					-230.3470064256034
				],
				[
					11.38345652832038,
					-230.3470064256034
				],
				[
					11.38345652832038,
					-231.6862125642578
				],
				[
					11.38345652832038,
					-231.0166094949306
				],
				[
					11.38345652832038,
					-231.0166094949306
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 567,
			"versionNonce": 706855037,
			"isDeleted": false,
			"id": "KhC0E30fnee8y39r5Iqfj",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -208.53172808573322,
			"y": -128.50461310324062,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 18.749192465798615,
			"height": 16.7403321703776,
			"seed": 1846558040,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.3392572260938778,
					0
				],
				[
					-2.008860295421073,
					0
				],
				[
					-3.348066434075463,
					0
				],
				[
					-4.017669503402658,
					0.6696286130469389
				],
				[
					-4.017669503402658,
					1.339231682374134
				],
				[
					-5.356926729496536,
					2.6784633647483247
				],
				[
					-6.026529798823844,
					3.3480664340755197
				],
				[
					-6.6961328681510395,
					4.017695047122459
				],
				[
					-8.035390094244917,
					4.017695047122459
				],
				[
					-8.035390094244917,
					5.356901185776849
				],
				[
					-8.704993163572112,
					6.026529798823844
				],
				[
					-10.044199302226502,
					7.365761481197978
				],
				[
					-10.044199302226502,
					8.035364550525173
				],
				[
					-10.713802371553697,
					8.035364550525173
				],
				[
					-10.713802371553697,
					9.374596232899364
				],
				[
					-11.38345652832038,
					9.374596232899364
				],
				[
					-11.38345652832038,
					10.04419930222656
				],
				[
					-10.713802371553697,
					10.04419930222656
				],
				[
					-9.374596232899307,
					8.704967619852368
				],
				[
					-9.374596232899307,
					8.035364550525173
				],
				[
					-8.704993163572112,
					8.035364550525173
				],
				[
					-8.704993163572112,
					6.6961328681510395
				],
				[
					-7.3657359374782345,
					6.026529798823844
				],
				[
					-6.6961328681510395,
					6.026529798823844
				],
				[
					-6.6961328681510395,
					4.687298116449654
				],
				[
					-6.026529798823844,
					4.017695047122459
				],
				[
					-4.687323660169341,
					4.017695047122459
				],
				[
					-4.687323660169341,
					3.3480664340755197
				],
				[
					-4.017669503402658,
					2.008834751701329
				],
				[
					-2.678463364748268,
					2.008834751701329
				],
				[
					-2.678463364748268,
					1.339231682374134
				],
				[
					-2.008860295421073,
					1.339231682374134
				],
				[
					-0.669603069327195,
					1.339231682374134
				],
				[
					0,
					1.339231682374134
				],
				[
					0.669603069327195,
					2.6784633647483247
				],
				[
					0.669603069327195,
					3.3480664340755197
				],
				[
					2.008809207981699,
					4.017695047122459
				],
				[
					2.008809207981699,
					5.356901185776849
				],
				[
					2.6784633647483815,
					6.026529798823844
				],
				[
					2.6784633647483815,
					7.365761481197978
				],
				[
					4.017669503402772,
					8.035364550525173
				],
				[
					4.017669503402772,
					9.374596232899364
				],
				[
					4.687272572729967,
					10.04419930222656
				],
				[
					4.687272572729967,
					10.713827915273498
				],
				[
					4.687272572729967,
					12.053034053927888
				],
				[
					6.026529798823844,
					12.722662666974884
				],
				[
					6.026529798823844,
					14.061894349349018
				],
				[
					6.6961328681510395,
					14.061894349349018
				],
				[
					6.6961328681510395,
					14.731497418676213
				],
				[
					6.6961328681510395,
					16.070729101050404
				],
				[
					7.3657359374782345,
					16.070729101050404
				],
				[
					7.3657359374782345,
					16.7403321703776
				],
				[
					7.3657359374782345,
					16.7403321703776
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 676,
			"versionNonce": 1379291603,
			"isDeleted": false,
			"id": "raeNhRC9",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 4.685211764148448,
			"x": -361.15310409253016,
			"y": -24.04495057757231,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 196.47988891601562,
			"height": 20,
			"seed": 1519698472,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "order of function calling ",
			"rawText": "order of function calling ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "order of function calling ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 573,
			"versionNonce": 1349429469,
			"isDeleted": false,
			"id": "npFLpPuP",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -246.18843142264427,
			"y": -215.5991908235253,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 223.10391235351562,
			"height": 35,
			"seed": 1303922264,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Stack Diagram :",
			"rawText": "Stack Diagram :",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Stack Diagram :",
			"lineHeight": 1.25
		},
		{
			"type": "ellipse",
			"version": 294,
			"versionNonce": 835886963,
			"isDeleted": false,
			"id": "d3pSoPPms5Yfghk18Rcw_",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -10.738510296717777,
			"y": -352.47969670861823,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 80.9803541126721,
			"height": 85.47926267448713,
			"seed": 2018884184,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "SVvj27Th"
				}
			],
			"updated": 1715421158211,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 214,
			"versionNonce": 29328701,
			"isDeleted": false,
			"id": "SVvj27Th",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 25.826789273377372,
			"y": -327.46154851535266,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 7.5879974365234375,
			"height": 35,
			"seed": 1198117720,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "1",
			"rawText": "1",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "d3pSoPPms5Yfghk18Rcw_",
			"originalText": "1",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1134,
			"versionNonce": 534001939,
			"isDeleted": false,
			"id": "6b9hE66MmkEPnsxP58Gfq",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -691.3536271672732,
			"y": 227.06776345551754,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 810.7795986610721,
			"height": 542.2523373967291,
			"seed": 827141464,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 394,
			"versionNonce": 561370525,
			"isDeleted": false,
			"id": "4sr8KmXfBce-D-14SeOuM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -5.935065332284466,
			"y": 250.6710867151446,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 80.9803541126721,
			"height": 85.47926267448713,
			"seed": 1226049112,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "HhGimhxq"
				}
			],
			"updated": 1715421158211,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 316,
			"versionNonce": 967941811,
			"isDeleted": false,
			"id": "HhGimhxq",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 24.456238266130995,
			"y": 275.6892349084102,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 19.935989379882812,
			"height": 35,
			"seed": 309427032,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "2",
			"rawText": "2",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4sr8KmXfBce-D-14SeOuM",
			"originalText": "2",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 870,
			"versionNonce": 717429245,
			"isDeleted": false,
			"id": "ChsdGppt",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -470.73804980055525,
			"y": 255.3885753132842,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 244.77589416503906,
			"height": 35,
			"seed": 1549546792,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "What is Recursion",
			"rawText": "What is Recursion",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "What is Recursion",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1068,
			"versionNonce": 705777747,
			"isDeleted": false,
			"id": "mKAysLFV",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -671.8074229498952,
			"y": 320.4038993122991,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 308.12786865234375,
			"height": 40,
			"seed": 542940456,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# Recursion is nothing but a condition \nin which a function calls itself...",
			"rawText": "# Recursion is nothing but a condition \nin which a function calls itself...",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# Recursion is nothing but a condition \nin which a function calls itself...",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1307,
			"versionNonce": 917033565,
			"isDeleted": false,
			"id": "TcZyPgAO",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -677.9262351206941,
			"y": 377.99503913760867,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 302.19183349609375,
			"height": 100,
			"seed": 1168966440,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# In recursion their must be a check \ncondition or base condition \nfor stopping the function from \ncalling itself when the \nrequirement is completed.  ",
			"rawText": "# In recursion their must be a check \ncondition or base condition \nfor stopping the function from \ncalling itself when the \nrequirement is completed.  ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# In recursion their must be a check \ncondition or base condition \nfor stopping the function from \ncalling itself when the \nrequirement is completed.  ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1858,
			"versionNonce": 46779891,
			"isDeleted": false,
			"id": "btlP4EgF",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -674.8889431759266,
			"y": 504.4153222846977,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 309.70941162109375,
			"height": 237.35526243962354,
			"seed": 1714832424,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 14.606477688592218,
			"fontFamily": 1,
			"text": "CODE Example : \n    public static void main(String[] args) {\n        print(1);\n    }    \n\n    static void print(int n){\n        if(n == 5){\n            System.out.println(n);\n            return;\n        }\n        System.out.println(n);\n        print(n+1);\n    }",
			"rawText": "CODE Example : \n    public static void main(String[] args) {\n        print(1);\n    }    \n\n    static void print(int n){\n        if(n == 5){\n            System.out.println(n);\n            return;\n        }\n        System.out.println(n);\n        print(n+1);\n    }",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CODE Example : \n    public static void main(String[] args) {\n        print(1);\n    }    \n\n    static void print(int n){\n        if(n == 5){\n            System.out.println(n);\n            return;\n        }\n        System.out.println(n);\n        print(n+1);\n    }",
			"lineHeight": 1.25
		},
		{
			"type": "line",
			"version": 1743,
			"versionNonce": 1106804413,
			"isDeleted": false,
			"id": "9WKuSxXc9VyyoJmvduogh",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -195.56419242588944,
			"y": 333.3473130676053,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.2298234385042677,
			"height": 179.55011713698184,
			"seed": 1215017256,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					-1.2298234385042677,
					179.55011713698184
				]
			]
		},
		{
			"type": "line",
			"version": 1803,
			"versionNonce": 1457624979,
			"isDeleted": false,
			"id": "lBJkprkY8BGFS5xCRPv7F",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -61.66033033510621,
			"y": 330.66151632887687,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.2298234385042677,
			"height": 179.55011713698184,
			"seed": 892029992,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					-1.2298234385042677,
					179.55011713698184
				]
			]
		},
		{
			"type": "line",
			"version": 1490,
			"versionNonce": 861118237,
			"isDeleted": false,
			"id": "mm8WcnpP0l0ChlgxijM4v",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -195.12211937684754,
			"y": 509.2335149931831,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 134.04770545408886,
			"height": 1.844664788305409,
			"seed": 1027573544,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					134.04770545408886,
					1.844664788305409
				]
			]
		},
		{
			"type": "freedraw",
			"version": 1006,
			"versionNonce": 344927539,
			"isDeleted": false,
			"id": "Nd_xSmzuGL-gnvZkw4g6h",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -197.22109410306643,
			"y": 485.80661393242025,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 131.5957429532267,
			"height": 1.3400786822285549,
			"seed": 1293181480,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.2680116468501177
				],
				[
					0.8040553885283195,
					-0.2680116468501177
				],
				[
					1.340078682228574,
					-0.2680116468501177
				],
				[
					2.680157364457129,
					-0.2680116468501177
				],
				[
					3.752224399835566,
					-0.2680116468501177
				],
				[
					6.164370117442558,
					-0.2680116468501177
				],
				[
					9.380550775599902,
					-0.2680116468501177
				],
				[
					13.13277517543545,
					0
				],
				[
					16.34897628157076,
					0
				],
				[
					19.565156939728105,
					0
				],
				[
					23.049369692713533,
					0
				],
				[
					26.801573644571153,
					0
				],
				[
					32.697932115163574,
					0
				],
				[
					36.986179808699355,
					0.5360232937002354
				],
				[
					41.81047124391334,
					0.5360232937002354
				],
				[
					46.634742231149396,
					0.5360232937002354
				],
				[
					51.45903366636338,
					0.5360232937002354
				],
				[
					56.28330465359944,
					0.5360232937002354
				],
				[
					60.839584441963304,
					0.5360232937002354
				],
				[
					65.66385542919932,
					0.5360232937002354
				],
				[
					69.95212357071307,
					0.5360232937002354
				],
				[
					74.24037126424885,
					0.5360232937002354
				],
				[
					77.99259566408439,
					0.5360232937002354
				],
				[
					81.4767879690919,
					0.5360232937002354
				],
				[
					84.6929890752272,
					0.5360232937002354
				],
				[
					87.37314643968432,
					0.5360232937002354
				],
				[
					90.85733874469177,
					0.5360232937002354
				],
				[
					92.4654290737705,
					0.5360232937002354
				],
				[
					95.41361853305564,
					1.0720670353784372
				],
				[
					97.02170886213432,
					1.0720670353784372
				],
				[
					98.89781083806315,
					1.0720670353784372
				],
				[
					100.50590116714181,
					1.0720670353784372
				],
				[
					102.65003523789869,
					1.0720670353784372
				],
				[
					103.72210227327713,
					1.0720670353784372
				],
				[
					105.33019260235581,
					1.0720670353784372
				],
				[
					106.13424799088412,
					1.0720670353784372
				],
				[
					106.40225963773425,
					1.0720670353784372
				],
				[
					107.47432667311267,
					1.0720670353784372
				],
				[
					108.27836161366302,
					1.0720670353784372
				],
				[
					108.54637326051315,
					1.0720670353784372
				],
				[
					109.88645194274174,
					1.0720670353784372
				],
				[
					110.15448403756979,
					1.0720670353784372
				],
				[
					110.95851897812014,
					1.0720670353784372
				],
				[
					111.76257436664847,
					1.0720670353784372
				],
				[
					112.03058601349858,
					1.0720670353784372
				],
				[
					113.37066469572713,
					1.0720670353784372
				],
				[
					113.90668798942741,
					1.0720670353784372
				],
				[
					114.71074337795568,
					1.0720670353784372
				],
				[
					115.514798766484,
					1.0720670353784372
				],
				[
					116.3188337070344,
					1.0720670353784372
				],
				[
					116.58684535388451,
					1.0720670353784372
				],
				[
					117.12288909556268,
					1.0720670353784372
				],
				[
					117.39090074241284,
					1.0720670353784372
				],
				[
					117.92692403611306,
					1.0720670353784372
				],
				[
					118.19495613094112,
					1.0720670353784372
				],
				[
					118.46296777779128,
					1.0720670353784372
				],
				[
					118.9989910714915,
					1.0720670353784372
				],
				[
					119.26700271834163,
					1.0720670353784372
				],
				[
					119.80304646001983,
					1.0720670353784372
				],
				[
					120.07105810686994,
					1.0720670353784372
				],
				[
					120.60708140057018,
					1.0720670353784372
				],
				[
					120.87511349539827,
					1.0720670353784372
				],
				[
					121.14312514224838,
					1.0720670353784372
				],
				[
					121.67914843594862,
					1.0720670353784372
				],
				[
					121.94716008279873,
					1.0720670353784372
				],
				[
					122.48320382447693,
					1.0720670353784372
				],
				[
					123.28723876502728,
					1.0720670353784372
				],
				[
					123.55527085985537,
					1.0720670353784372
				],
				[
					124.35930580040572,
					1.0720670353784372
				],
				[
					124.62731744725585,
					1.0720670353784372
				],
				[
					125.16336118893405,
					1.0720670353784372
				],
				[
					125.69938448263429,
					1.0720670353784372
				],
				[
					126.23542822431249,
					1.0720670353784372
				],
				[
					126.5034398711626,
					1.0720670353784372
				],
				[
					127.30747481171295,
					1.0720670353784372
				],
				[
					127.84351855339115,
					1.0720670353784372
				],
				[
					128.11153020024128,
					1.0720670353784372
				],
				[
					128.3795418470914,
					1.0720670353784372
				],
				[
					128.9155855887696,
					1.0720670353784372
				],
				[
					129.18359723561971,
					1.0720670353784372
				],
				[
					129.71962052931994,
					1.0720670353784372
				],
				[
					129.9876321761701,
					1.0720670353784372
				],
				[
					130.52367591784827,
					1.0720670353784372
				],
				[
					130.79168756469838,
					1.0720670353784372
				],
				[
					131.0596992115485,
					1.0720670353784372
				],
				[
					131.5957429532267,
					1.0720670353784372
				],
				[
					131.5957429532267,
					1.0720670353784372
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 992,
			"versionNonce": 556512125,
			"isDeleted": false,
			"id": "kYorRBqw-rfeatLGaR6h1",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -196.9530620082384,
			"y": 464.2983469930563,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 136.15198184563468,
			"height": 1.6080903290786726,
			"seed": 1670765864,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.5360232937002354
				],
				[
					0,
					-0.804034940550353
				],
				[
					0.5360232937002544,
					-0.804034940550353
				],
				[
					0.804034940550372,
					-0.804034940550353
				],
				[
					1.3400786822285737,
					-0.804034940550353
				],
				[
					1.876101975928809,
					-0.804034940550353
				],
				[
					2.6801573644571284,
					-0.804034940550353
				],
				[
					3.4841923050075003,
					-1.0720670353784372
				],
				[
					5.092282634086172,
					-1.6080903290786726
				],
				[
					9.112518680771837,
					-1.6080903290786726
				],
				[
					10.720629457828474,
					-1.6080903290786726
				],
				[
					15.276888798214374,
					-1.6080903290786726
				],
				[
					19.02911319804992,
					-1.6080903290786726
				],
				[
					22.781337597885464,
					-1.6080903290786726
				],
				[
					27.069585291421284,
					-1.6080903290786726
				],
				[
					31.357832984957067,
					-1.6080903290786726
				],
				[
					35.64608067849285,
					-1.6080903290786726
				],
				[
					40.47037211370683,
					-1.6080903290786726
				],
				[
					44.75861980724265,
					-1.6080903290786726
				],
				[
					49.58291124245663,
					-1.6080903290786726
				],
				[
					53.87115893599241,
					-1.6080903290786726
				],
				[
					57.62338333582796,
					-1.6080903290786726
				],
				[
					61.375587287685576,
					-1.6080903290786726
				],
				[
					64.59178839382089,
					-1.6080903290786726
				],
				[
					67.00393411142788,
					-1.6080903290786726
				],
				[
					69.14804773420678,
					-1.6080903290786726
				],
				[
					70.75613806328546,
					-1.6080903290786726
				],
				[
					71.8282050986639,
					-1.6080903290786726
				],
				[
					72.63226048719221,
					-1.6080903290786726
				],
				[
					74.24035081627089,
					-1.6080903290786726
				],
				[
					74.50836246312105,
					-1.6080903290786726
				],
				[
					75.0444062047992,
					-1.6080903290786726
				],
				[
					75.31241785164933,
					-1.6080903290786726
				],
				[
					75.58042949849944,
					-1.6080903290786726
				],
				[
					76.11645279219972,
					-1.6080903290786726
				],
				[
					76.38448488702777,
					-1.6080903290786726
				],
				[
					76.92050818072804,
					-1.6080903290786726
				],
				[
					77.72456356925632,
					-1.6080903290786726
				],
				[
					78.79661015665683,
					-1.6080903290786726
				],
				[
					80.67273258056358,
					-1.6080903290786726
				],
				[
					82.54883455649237,
					-1.3400786822285549
				],
				[
					84.96098027409937,
					-1.3400786822285549
				],
				[
					86.0330473094778,
					-1.3400786822285549
				],
				[
					88.98121632078502,
					-1.0720670353784372
				],
				[
					91.1253503915419,
					-1.0720670353784372
				],
				[
					94.07351940284913,
					-1.0720670353784372
				],
				[
					96.75367676730623,
					-1.0720670353784372
				],
				[
					100.50590116714179,
					-1.0720670353784372
				],
				[
					104.2581051189994,
					-1.0720670353784372
				],
				[
					108.01032951883495,
					-1.0720670353784372
				],
				[
					111.76255391867049,
					-0.5360232937002354
				],
				[
					116.05080161220631,
					-0.5360232937002354
				],
				[
					119.80302601204185,
					-0.5360232937002354
				],
				[
					123.28723876502728,
					-0.5360232937002354
				],
				[
					125.9673961294844,
					-0.5360232937002354
				],
				[
					129.18357678764175,
					-0.5360232937002354
				],
				[
					131.59572250524874,
					-0.5360232937002354
				],
				[
					133.7398361280277,
					-0.5360232937002354
				],
				[
					134.543891516556,
					-0.5360232937002354
				],
				[
					134.81190316340613,
					-0.5360232937002354
				],
				[
					135.34794690508429,
					-0.5360232937002354
				],
				[
					135.6159585519344,
					-0.5360232937002354
				],
				[
					136.15198184563468,
					-0.5360232937002354
				],
				[
					135.88397019878454,
					0
				],
				[
					135.6159585519344,
					0
				],
				[
					135.07991481025624,
					0
				],
				[
					134.81190316340613,
					0
				],
				[
					134.27587986970585,
					0
				],
				[
					134.00786822285573,
					0
				],
				[
					134.00786822285573,
					-0.2680116468501177
				],
				[
					133.7398361280277,
					-0.2680116468501177
				],
				[
					133.7398361280277,
					-0.5360232937002354
				],
				[
					133.7398361280277,
					-0.5360232937002354
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 1020,
			"versionNonce": 523833043,
			"isDeleted": false,
			"id": "XgwxWF5YpqJnD3NfNFhbN",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -195.61298332600978,
			"y": 439.1048636775639,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 130.79166711672045,
			"height": 1.0720670353784372,
			"seed": 1110439976,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.2680116468501177,
					0
				],
				[
					1.0720465874004899,
					0
				],
				[
					1.8761019759288093,
					0
				],
				[
					2.9481690113072463,
					0
				],
				[
					4.020236046685645,
					0
				],
				[
					5.628326375764356,
					0
				],
				[
					7.7724399985432635,
					0
				],
				[
					10.452597363000374,
					0
				],
				[
					13.400786822285568,
					0
				],
				[
					16.616967480442913,
					0
				],
				[
					20.369191880278457,
					0
				],
				[
					24.65743957381428,
					0
				],
				[
					29.481731009028262,
					0
				],
				[
					34.30600199626428,
					0
				],
				[
					39.93432837202865,
					0.2680320948280841
				],
				[
					44.75861980724264,
					0.2680320948280841
				],
				[
					51.459013218385415,
					0.2680320948280841
				],
				[
					57.62338333582795,
					0.8040553885283195
				],
				[
					62.71566596991413,
					0.8040553885283195
				],
				[
					68.34401279365643,
					0.8040553885283195
				],
				[
					72.09621674551404,
					0.8040553885283195
				],
				[
					74.50836246312103,
					0.8040553885283195
				],
				[
					76.11645279219971,
					0.8040553885283195
				],
				[
					77.45653147442826,
					0.8040553885283195
				],
				[
					77.99257521610643,
					0.8040553885283195
				],
				[
					78.79661015665683,
					0.8040553885283195
				],
				[
					79.33265389833502,
					0.8040553885283195
				],
				[
					79.60066554518514,
					0.8040553885283195
				],
				[
					80.13668883888538,
					0.8040553885283195
				],
				[
					80.40472093371342,
					0.8040553885283195
				],
				[
					81.47676752111393,
					1.0720670353784372
				],
				[
					82.54883455649237,
					1.0720670353784372
				],
				[
					84.15692488557104,
					1.0720670353784372
				],
				[
					85.4970035677996,
					1.0720670353784372
				],
				[
					87.37312599170635,
					1.0720670353784372
				],
				[
					90.5893066498637,
					1.0720670353784372
				],
				[
					93.53747566117096,
					1.0720670353784372
				],
				[
					95.14558643822757,
					1.0720670353784372
				],
				[
					96.75367676730623,
					1.0720670353784372
				],
				[
					97.55771170785663,
					1.0720670353784372
				],
				[
					98.09375544953483,
					1.0720670353784372
				],
				[
					98.89779039008518,
					1.0720670353784372
				],
				[
					99.7018457786135,
					1.0720670353784372
				],
				[
					100.23786907231373,
					1.0720670353784372
				],
				[
					100.50590116714181,
					1.0720670353784372
				],
				[
					100.77391281399194,
					1.0720670353784372
				],
				[
					101.30993610769217,
					1.0720670353784372
				],
				[
					101.5779477545423,
					1.0720670353784372
				],
				[
					102.11399149622049,
					1.0720670353784372
				],
				[
					102.3820031430706,
					1.0720670353784372
				],
				[
					103.18605853159893,
					1.0720670353784372
				],
				[
					103.45407017844904,
					1.0720670353784372
				],
				[
					104.7941488606776,
					1.0720670353784372
				],
				[
					105.86621589605603,
					1.0720670353784372
				],
				[
					106.93826248345651,
					1.0720670353784372
				],
				[
					108.54637326051315,
					1.0720670353784372
				],
				[
					109.61841984791366,
					1.0720670353784372
				],
				[
					110.95849853014221,
					1.0720670353784372
				],
				[
					112.03056556552065,
					1.0720670353784372
				],
				[
					113.10263260089904,
					1.0720670353784372
				],
				[
					113.90668798942737,
					1.0720670353784372
				],
				[
					114.71072292997776,
					1.0720670353784372
				],
				[
					115.51477831850605,
					1.0720670353784372
				],
				[
					116.05080161220631,
					1.0720670353784372
				],
				[
					116.58684535388447,
					1.0720670353784372
				],
				[
					116.85485700073463,
					1.0720670353784372
				],
				[
					117.39088029443487,
					1.0720670353784372
				],
				[
					117.65889194128499,
					1.0720670353784372
				],
				[
					118.19493568296319,
					1.0720670353784372
				],
				[
					118.4629473298133,
					1.0720670353784372
				],
				[
					118.73095897666342,
					1.0720670353784372
				],
				[
					119.26700271834163,
					1.0720670353784372
				],
				[
					119.53501436519174,
					1.0720670353784372
				],
				[
					120.07103765889198,
					1.0720670353784372
				],
				[
					120.3390493057421,
					1.0720670353784372
				],
				[
					120.8750930474203,
					1.0720670353784372
				],
				[
					121.14310469427042,
					1.0720670353784372
				],
				[
					121.41111634112053,
					1.0720670353784372
				],
				[
					121.94716008279873,
					1.0720670353784372
				],
				[
					122.21517172964886,
					1.0720670353784372
				],
				[
					122.75119502334908,
					1.0720670353784372
				],
				[
					123.01920667019921,
					1.0720670353784372
				],
				[
					123.28723876502728,
					1.0720670353784372
				],
				[
					123.82326205872752,
					1.0720670353784372
				],
				[
					124.09127370557763,
					1.0720670353784372
				],
				[
					124.89532909410596,
					1.0720670353784372
				],
				[
					125.69936403465631,
					1.0720670353784372
				],
				[
					125.9673961294844,
					1.0720670353784372
				],
				[
					126.50341942318464,
					1.0720670353784372
				],
				[
					126.77143107003475,
					1.0720670353784372
				],
				[
					127.30747481171295,
					1.0720670353784372
				],
				[
					127.57548645856308,
					1.0720670353784372
				],
				[
					128.37952139911346,
					1.0720670353784372
				],
				[
					128.6475534939415,
					1.0720670353784372
				],
				[
					129.18357678764175,
					1.0720670353784372
				],
				[
					129.45158843449187,
					1.0720670353784372
				],
				[
					129.98763217617005,
					1.0720670353784372
				],
				[
					130.2556438230202,
					1.0720670353784372
				],
				[
					130.79166711672045,
					1.0720670353784372
				],
				[
					130.5236554698703,
					1.0720670353784372
				],
				[
					130.5236554698703,
					1.0720670353784372
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 1024,
			"versionNonce": 1472347101,
			"isDeleted": false,
			"id": "ougIgahe8HQUAIyBcN6sq",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -194.80894838545944,
			"y": 410.4271880570639,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 130.79168756469838,
			"height": 1.87610197592879,
			"seed": 483308328,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.8040553885283195,
					0
				],
				[
					1.6080903290786916,
					0
				],
				[
					2.412145717607011,
					0
				],
				[
					3.2162011061352924,
					0
				],
				[
					3.752224399835566,
					0
				],
				[
					5.09230308206412,
					0
				],
				[
					6.164370117442558,
					0.2680116468501177
				],
				[
					7.2364371528209945,
					0.2680116468501177
				],
				[
					8.308483740221465,
					0.2680116468501177
				],
				[
					9.64856242245002,
					0.2680116468501177
				],
				[
					10.720629457828457,
					0.2680116468501177
				],
				[
					12.328719786907168,
					0.2680116468501177
				],
				[
					13.936830563963769,
					0.2680116468501177
				],
				[
					15.812932539892559,
					0.2680116468501177
				],
				[
					17.42102286897127,
					0.2680116468501177
				],
				[
					19.83316858657826,
					0.2680116468501177
				],
				[
					21.441258915656935,
					0.2680116468501177
				],
				[
					23.317381339563692,
					0.2680116468501177
				],
				[
					24.657460021792247,
					0.2680116468501177
				],
				[
					27.06958529142127,
					0.2680116468501177
				],
				[
					28.945707715328027,
					0.2680116468501177
				],
				[
					31.089821338106972,
					0.2680116468501177
				],
				[
					32.697932115163574,
					0.2680116468501177
				],
				[
					34.574034091092365,
					0.2680116468501177
				],
				[
					36.18212442017107,
					0.2680116468501177
				],
				[
					38.32625849092791,
					0.2680116468501177
				],
				[
					40.20236046685674,
					0.2680116468501177
				],
				[
					42.346494537613616,
					0.2680116468501177
				],
				[
					44.49060816039252,
					0.2680116468501177
				],
				[
					47.438797619677715,
					0.2680116468501177
				],
				[
					50.118954984134824,
					0.2680116468501177
				],
				[
					52.53108025376389,
					0.2680116468501177
				],
				[
					54.675214324520724,
					0.2680116468501177
				],
				[
					56.8193483952776,
					0.2680116468501177
				],
				[
					58.42743872435631,
					0.2680116468501177
				],
				[
					60.3035407002851,
					0.2680116468501177
				],
				[
					61.91163102936377,
					0.2680116468501177
				],
				[
					62.98369806474221,
					0.2680116468501177
				],
				[
					64.59178839382088,
					0.2680116468501177
				],
				[
					65.66385542919932,
					0.2680116468501177
				],
				[
					66.46791081772764,
					0.2680116468501177
				],
				[
					67.271945758278,
					0.2680116468501177
				],
				[
					68.34401279365643,
					0.2680116468501177
				],
				[
					69.14806818218474,
					0.2680116468501177
				],
				[
					69.95210312273514,
					0.2680116468501177
				],
				[
					71.02417015811353,
					0.2680116468501177
				],
				[
					71.82822554664186,
					0.2680116468501177
				],
				[
					73.43631587572052,
					0.2680116468501177
				],
				[
					74.50838291109896,
					0.2680116468501177
				],
				[
					75.5804499464774,
					0.2680116468501177
				],
				[
					76.92052862870595,
					0.2680116468501177
				],
				[
					78.26060731093452,
					0.2680116468501177
				],
				[
					79.60068599316307,
					0.2680116468501177
				],
				[
					81.20877632224177,
					0.2680116468501177
				],
				[
					82.28084335762021,
					0.2680116468501177
				],
				[
					83.88893368669889,
					0.2680116468501177
				],
				[
					84.96100072207733,
					0.2680116468501177
				],
				[
					86.569091051156,
					0.2680116468501177
				],
				[
					87.64115808653443,
					0.2680116468501177
				],
				[
					89.24924841561311,
					0.2680116468501177
				],
				[
					90.32131545099155,
					0.2680116468501177
				],
				[
					91.92940578007021,
					0.2680116468501177
				],
				[
					94.07351940284916,
					0.8040553885283003
				],
				[
					97.02170886213432,
					0.8040553885283003
				],
				[
					102.38202359104858,
					0.8040553885283003
				],
				[
					103.18605853159893,
					0.8040553885283003
				],
				[
					104.7941488606776,
					0.8040553885283003
				],
				[
					107.47430622513475,
					1.3400786822285549
				],
				[
					110.15446358959186,
					1.3400786822285549
				],
				[
					112.56660930719885,
					1.3400786822285549
				],
				[
					114.71074337795568,
					1.3400786822285549
				],
				[
					116.58684535388451,
					1.3400786822285549
				],
				[
					117.92692403611306,
					1.3400786822285549
				],
				[
					118.73097942464139,
					1.3400786822285549
				],
				[
					119.26700271834163,
					1.3400786822285549
				],
				[
					119.80304646001983,
					1.3400786822285549
				],
				[
					120.07105810686994,
					1.3400786822285549
				],
				[
					120.60708140057018,
					1.3400786822285549
				],
				[
					120.8750930474203,
					1.3400786822285549
				],
				[
					121.41113678909849,
					1.3400786822285549
				],
				[
					121.67914843594862,
					1.3400786822285549
				],
				[
					121.94716008279873,
					1.6080903290786726
				],
				[
					122.48320382447693,
					1.6080903290786726
				],
				[
					122.75121547132706,
					1.6080903290786726
				],
				[
					123.28723876502728,
					1.6080903290786726
				],
				[
					123.55525041187741,
					1.6080903290786726
				],
				[
					123.8232825067055,
					1.6080903290786726
				],
				[
					124.35930580040572,
					1.6080903290786726
				],
				[
					124.62731744725585,
					1.6080903290786726
				],
				[
					125.16336118893405,
					1.6080903290786726
				],
				[
					125.43137283578416,
					1.6080903290786726
				],
				[
					125.9673961294844,
					1.6080903290786726
				],
				[
					126.23540777633451,
					1.6080903290786726
				],
				[
					126.5034398711626,
					1.6080903290786726
				],
				[
					127.03946316486284,
					1.6080903290786726
				],
				[
					127.30747481171295,
					1.6080903290786726
				],
				[
					128.11153020024128,
					1.6080903290786726
				],
				[
					128.6475534939415,
					1.87610197592879
				],
				[
					128.91556514079167,
					1.87610197592879
				],
				[
					129.18359723561971,
					1.87610197592879
				],
				[
					129.71962052931994,
					1.87610197592879
				],
				[
					129.9876321761701,
					1.87610197592879
				],
				[
					130.52367591784827,
					1.87610197592879
				],
				[
					130.79168756469838,
					1.87610197592879
				],
				[
					130.79168756469838,
					1.87610197592879
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 1025,
			"versionNonce": 695581811,
			"isDeleted": false,
			"id": "HV0E1MI4oI-aVCmqwNo1y",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -195.61298332600978,
			"y": 383.3575925416537,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 129.719600081342,
			"height": 0.8040451645393363,
			"seed": 1239289384,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.5360232937002354,
					0
				],
				[
					0.804034940550353,
					0
				],
				[
					1.6080903290786726,
					0
				],
				[
					2.6801573644570906,
					-0.5360232937002354
				],
				[
					4.020236046685645,
					-0.5360232937002354
				],
				[
					5.092282634086154,
					-0.8040451645393363
				],
				[
					6.164349669464591,
					-0.8040451645393363
				],
				[
					7.7724399985432635,
					-0.8040451645393363
				],
				[
					10.988641104678575,
					-0.8040451645393363
				],
				[
					14.20482176283592,
					-0.8040451645393363
				],
				[
					17.152990774143184,
					-0.8040451645393363
				],
				[
					20.905215173978732,
					-0.8040451645393363
				],
				[
					24.65743957381428,
					-0.8040451645393363
				],
				[
					29.481731009028262,
					-0.8040451645393363
				],
				[
					34.30600199626428,
					-0.8040451645393363
				],
				[
					39.130293431478265,
					-0.8040451645393363
				],
				[
					44.75861980724264,
					-0.8040451645393363
				],
				[
					50.11893453615686,
					-0.8040451645393363
				],
				[
					55.479249265071076,
					-0.8040451645393363
				],
				[
					60.57155234713522,
					-0.8040451645393363
				],
				[
					65.39582333437123,
					-0.8040451645393363
				],
				[
					69.68409147588498,
					-0.8040451645393363
				],
				[
					73.97233916942076,
					-0.8040451645393363
				],
				[
					79.33265389833502,
					-0.8040451645393363
				],
				[
					80.40472093371342,
					-0.8040451645393363
				],
				[
					82.54883455649237,
					-0.8040451645393363
				],
				[
					83.35288994502069,
					-0.8040451645393363
				],
				[
					83.6209015918708,
					-0.8040451645393363
				],
				[
					84.15692488557104,
					-0.8040451645393363
				],
				[
					84.42495698039912,
					-0.8040451645393363
				],
				[
					84.96098027409936,
					-0.8040451645393363
				],
				[
					85.22899192094948,
					-0.8040451645393363
				],
				[
					86.0330473094778,
					-0.8040451645393363
				],
				[
					86.83708225002815,
					-0.8040451645393363
				],
				[
					87.90914928540658,
					-0.8040451645393363
				],
				[
					88.98121632078502,
					-0.8040451645393363
				],
				[
					90.32129500301357,
					-0.8040451645393363
				],
				[
					91.39336203839201,
					-0.8040451645393363
				],
				[
					92.46542907377045,
					-0.8040451645393363
				],
				[
					93.53747566117096,
					-0.8040451645393363
				],
				[
					94.87755434339951,
					-0.8040451645393363
				],
				[
					95.94962137877795,
					-0.8040451645393363
				],
				[
					97.02168841415639,
					-0.8040451645393363
				],
				[
					97.82574380268467,
					-0.8040451645393363
				],
				[
					98.89779039008518,
					-0.8040451645393363
				],
				[
					99.7018457786135,
					-0.8040451645393363
				],
				[
					100.77391281399194,
					-0.8040451645393363
				],
				[
					101.5779477545423,
					-0.8040451645393363
				],
				[
					102.65001478992073,
					-0.8040451645393363
				],
				[
					103.18605853159893,
					-0.8040451645393363
				],
				[
					104.2581051189994,
					-0.8040451645393363
				],
				[
					105.06216050752772,
					-0.8040451645393363
				],
				[
					105.33017215437783,
					-0.8040451645393363
				],
				[
					106.93826248345651,
					-0.8040451645393363
				],
				[
					107.74231787198482,
					-0.8040451645393363
				],
				[
					108.81438490736326,
					-0.8040451645393363
				],
				[
					109.61841984791366,
					-0.8040451645393363
				],
				[
					110.42247523644194,
					-0.8040451645393363
				],
				[
					111.49454227182038,
					-0.8040451645393363
				],
				[
					112.03056556552065,
					-0.8040451645393363
				],
				[
					112.29857721237076,
					-0.8040451645393363
				],
				[
					112.56660930719882,
					-0.8040451645393363
				],
				[
					113.10263260089904,
					-0.8040451645393363
				],
				[
					113.3706442477492,
					-0.8040451645393363
				],
				[
					113.90668798942737,
					-0.8040451645393363
				],
				[
					114.17469963627748,
					-0.8040451645393363
				],
				[
					114.71072292997776,
					-0.8040451645393363
				],
				[
					114.97873457682788,
					-0.8040451645393363
				],
				[
					115.24676667165592,
					-0.8040451645393363
				],
				[
					115.7827899653562,
					-0.8040451645393363
				],
				[
					116.05080161220631,
					-0.8040451645393363
				],
				[
					116.58684535388447,
					-0.8040451645393363
				],
				[
					116.85485700073463,
					-0.8040451645393363
				],
				[
					117.39088029443487,
					-0.8040451645393363
				],
				[
					117.65889194128499,
					-0.8040451645393363
				],
				[
					117.92692403611304,
					-0.8040451645393363
				],
				[
					118.4629473298133,
					-0.8040451645393363
				],
				[
					118.73095897666342,
					-0.8040451645393363
				],
				[
					119.26700271834163,
					-0.8040451645393363
				],
				[
					119.53501436519174,
					-0.8040451645393363
				],
				[
					119.80302601204185,
					-0.8040451645393363
				],
				[
					120.3390493057421,
					-0.8040451645393363
				],
				[
					120.60708140057018,
					-0.8040451645393363
				],
				[
					121.14310469427042,
					-0.8040451645393363
				],
				[
					121.41111634112053,
					-0.8040451645393363
				],
				[
					122.21517172964886,
					-0.8040451645393363
				],
				[
					122.48318337649897,
					-0.8040451645393363
				],
				[
					123.01920667019921,
					-0.8040451645393363
				],
				[
					123.82326205872752,
					-0.8040451645393363
				],
				[
					124.09127370557763,
					-0.8040451645393363
				],
				[
					124.62731744725585,
					-0.8040451645393363
				],
				[
					124.89532909410596,
					-0.8040451645393363
				],
				[
					125.16334074095607,
					-0.8040451645393363
				],
				[
					125.69936403465631,
					-0.8040451645393363
				],
				[
					125.9673961294844,
					-0.8040451645393363
				],
				[
					126.50341942318464,
					-0.8040451645393363
				],
				[
					126.77143107003475,
					-0.8040451645393363
				],
				[
					127.03944271688486,
					-0.8040451645393363
				],
				[
					127.57548645856308,
					-0.8040451645393363
				],
				[
					127.84349810541319,
					-0.8040451645393363
				],
				[
					128.37952139911346,
					-0.8040451645393363
				],
				[
					128.6475534939415,
					-0.8040451645393363
				],
				[
					129.18357678764175,
					-0.8040451645393363
				],
				[
					129.45158843449187,
					-0.8040451645393363
				],
				[
					129.719600081342,
					-0.8040451645393363
				],
				[
					129.719600081342,
					-0.8040451645393363
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 1025,
			"versionNonce": 522762301,
			"isDeleted": false,
			"id": "HpPXjPH2X4UpKLoYCrzQp",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -195.34497167915967,
			"y": 354.0768753797575,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 132.39977789377704,
			"height": 2.948169011307227,
			"seed": 1917454632,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.5360335176892186
				],
				[
					0.26801164685011764,
					-0.5360335176892186
				],
				[
					0.5360232937002353,
					-0.5360335176892186
				],
				[
					1.3400786822285546,
					-0.5360335176892186
				],
				[
					2.1441136227789266,
					-0.5360335176892186
				],
				[
					2.948169011307246,
					-0.5360335176892186
				],
				[
					3.752224399835527,
					-0.5360335176892186
				],
				[
					4.556259340385918,
					-0.5360335176892186
				],
				[
					6.16434966946459,
					-0.5360335176892186
				],
				[
					8.576495387071581,
					-0.5360335176892186
				],
				[
					11.792696493206893,
					-0.5360335176892186
				],
				[
					14.204821762835955,
					-0.5360335176892186
				],
				[
					17.421022868971228,
					-0.5360335176892186
				],
				[
					21.173247268806776,
					-0.5360335176892186
				],
				[
					24.925451220664392,
					-0.5360335176892186
				],
				[
					29.21371936217814,
					-0.5360335176892186
				],
				[
					32.965923314035756,
					-0.5360335176892186
				],
				[
					36.7181477138713,
					-0.5360335176892186
				],
				[
					40.47037211370685,
					-1.072056811389454
				],
				[
					45.56267519577095,
					-1.072056811389454
				],
				[
					48.77885585392829,
					-1.072056811389454
				],
				[
					51.72702486523556,
					-1.072056811389454
				],
				[
					54.40718222969267,
					-1.072056811389454
				],
				[
					56.55131630044954,
					-1.072056811389454
				],
				[
					57.8913949826781,
					-1.072056811389454
				],
				[
					59.23147366490665,
					-1.072056811389454
				],
				[
					59.767496958606884,
					-1.072056811389454
				],
				[
					60.57155234713521,
					-1.072056811389454
				],
				[
					61.375607735663486,
					-1.072056811389454
				],
				[
					62.17964267621388,
					-1.072056811389454
				],
				[
					62.44765432306399,
					-1.072056811389454
				],
				[
					63.25170971159232,
					-1.072056811389454
				],
				[
					64.05576510012064,
					-1.072056811389454
				],
				[
					65.1278116875211,
					-1.072056811389454
				],
				[
					66.46789036974965,
					-1.072056811389454
				],
				[
					67.53995740512809,
					-1.072056811389454
				],
				[
					69.68409147588497,
					-1.072056811389454
				],
				[
					72.09623719349196,
					-1.072056811389454
				],
				[
					74.77639455794908,
					-0.8040451645393363
				],
				[
					77.45655192240618,
					-0.8040451645393363
				],
				[
					79.86867719203525,
					-0.8040451645393363
				],
				[
					82.54883455649235,
					-0.2680116468501177
				],
				[
					85.22899192094947,
					-0.2680116468501177
				],
				[
					87.64113763855646,
					-0.2680116468501177
				],
				[
					89.78527170931332,
					-0.2680116468501177
				],
				[
					91.393362038392,
					-0.2680116468501177
				],
				[
					93.26946401432083,
					-0.2680116468501177
				],
				[
					94.87757479137743,
					-0.2680116468501177
				],
				[
					96.4856651204561,
					-0.2680116468501177
				],
				[
					97.28970006100649,
					0
				],
				[
					97.8257438026847,
					0
				],
				[
					98.09375544953481,
					0
				],
				[
					98.36176709638492,
					0
				],
				[
					98.8978108380631,
					0
				],
				[
					99.16582248491325,
					0
				],
				[
					99.70184577861349,
					0
				],
				[
					100.23788952029169,
					0
				],
				[
					101.57796820252024,
					0
				],
				[
					102.38200314307059,
					0.2680218708391009
				],
				[
					103.72208182529914,
					0.2680218708391009
				],
				[
					105.06216050752771,
					0.8040451645393554
				],
				[
					106.67025083660637,
					0.8040451645393554
				],
				[
					108.01032951883496,
					1.0720670353784372
				],
				[
					109.61844029589156,
					1.0720670353784372
				],
				[
					111.22653062497024,
					1.0720670353784372
				],
				[
					112.83462095404892,
					1.6081005530676558
				],
				[
					113.90668798942735,
					1.6081005530676558
				],
				[
					115.2467666716559,
					1.6081005530676558
				],
				[
					116.31883370703434,
					1.6081005530676558
				],
				[
					117.92692403611305,
					1.6081005530676558
				],
				[
					118.19493568296316,
					1.6081005530676558
				],
				[
					118.7309589766634,
					1.6081005530676558
				],
				[
					119.2670027183416,
					1.6081005530676558
				],
				[
					119.80302601204184,
					1.6081005530676558
				],
				[
					120.07103765889195,
					1.6081005530676558
				],
				[
					120.60708140057015,
					1.6081005530676558
				],
				[
					120.87509304742028,
					1.6081005530676558
				],
				[
					121.41111634112052,
					1.6081005530676558
				],
				[
					121.67914843594859,
					1.6081005530676558
				],
				[
					121.94716008279872,
					1.8761121999177734
				],
				[
					122.48318337649894,
					1.8761121999177734
				],
				[
					122.75119502334907,
					1.8761121999177734
				],
				[
					123.28723876502727,
					1.8761121999177734
				],
				[
					123.55525041187738,
					1.8761121999177734
				],
				[
					123.82326205872751,
					1.8761121999177734
				],
				[
					124.3593058004057,
					1.8761121999177734
				],
				[
					124.62731744725582,
					1.8761121999177734
				],
				[
					125.16334074095606,
					1.8761121999177734
				],
				[
					125.43135238780617,
					1.8761121999177734
				],
				[
					125.96739612948437,
					1.8761121999177734
				],
				[
					126.2354077763345,
					1.8761121999177734
				],
				[
					126.50341942318461,
					1.8761121999177734
				],
				[
					127.03946316486281,
					1.8761121999177734
				],
				[
					127.30747481171294,
					1.8761121999177734
				],
				[
					127.84349810541316,
					1.8761121999177734
				],
				[
					128.11150975226332,
					1.8761121999177734
				],
				[
					128.64755349394147,
					1.8761121999177734
				],
				[
					129.18357678764173,
					1.8761121999177734
				],
				[
					129.7196205293199,
					1.8761121999177734
				],
				[
					129.98763217617005,
					1.8761121999177734
				],
				[
					130.79166711672042,
					1.8761121999177734
				],
				[
					131.0596992115485,
					1.8761121999177734
				],
				[
					131.59572250524872,
					1.8761121999177734
				],
				[
					131.86373415209886,
					1.8761121999177734
				],
				[
					132.39977789377704,
					1.8761121999177734
				],
				[
					132.39977789377704,
					1.8761121999177734
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 945,
			"versionNonce": 1326167571,
			"isDeleted": false,
			"id": "XafBksFh",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -145.54040869153232,
			"y": 490.83190899077744,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 21.36932373046875,
			"height": 13.45817433623004,
			"seed": 1098818600,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158211,
			"link": null,
			"locked": false,
			"fontSize": 10.766539468984032,
			"fontFamily": 1,
			"text": "main",
			"rawText": "main",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "main",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 938,
			"versionNonce": 1094756509,
			"isDeleted": false,
			"id": "4L3RXsJP",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -156.46828492792815,
			"y": 468.31860348771994,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 42.70635986328125,
			"height": 13.45817433623004,
			"seed": 359128872,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 10.766539468984032,
			"fontFamily": 1,
			"text": "print1 (1)",
			"rawText": "print1 (1)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print1 (1)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1025,
			"versionNonce": 1861319603,
			"isDeleted": false,
			"id": "JEmSLaV8",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -170.8406706446142,
			"y": 443.2974300383983,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 52.196685791015625,
			"height": 13.45817433623004,
			"seed": 779205160,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 10.766539468984032,
			"fontFamily": 1,
			"text": "print2 (2)",
			"rawText": "print2 (2)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print2 (2)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1047,
			"versionNonce": 1337691389,
			"isDeleted": false,
			"id": "oP8Ij74R",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -170.39217877678573,
			"y": 388.75622153730274,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 50.647247314453125,
			"height": 13.45817433623004,
			"seed": 1602762024,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 10.766539468984032,
			"fontFamily": 1,
			"text": "print4 (4)",
			"rawText": "print4 (4)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print4 (4)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1014,
			"versionNonce": 1162710355,
			"isDeleted": false,
			"id": "NsqZtrOM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -170.50980100824006,
			"y": 417.9029430997628,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 51.529541015625,
			"height": 13.45817433623004,
			"seed": 1041715240,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 10.766539468984032,
			"fontFamily": 1,
			"text": "print3 (3)",
			"rawText": "print3 (3)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print3 (3)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1018,
			"versionNonce": 706405725,
			"isDeleted": false,
			"id": "9iuGjqpg",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -167.6047153385798,
			"y": 362.42367338671374,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 50.173797607421875,
			"height": 13.45817433623004,
			"seed": 1376455464,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 10.766539468984032,
			"fontFamily": 1,
			"text": "print5 (5)",
			"rawText": "print5 (5)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print5 (5)",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 928,
			"versionNonce": 1165388531,
			"isDeleted": false,
			"id": "-U39u4rHC-nSAtPHlqoXv",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -168.42421059477329,
			"y": 377.2182086461806,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 59.928299890434346,
			"height": 10.81413369761309,
			"seed": 1171220008,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.9011634843080886,
					0
				],
				[
					1.3517796036454455,
					0
				],
				[
					2.7035248301074635,
					0
				],
				[
					4.055304433752832,
					0
				],
				[
					5.857665779552284,
					-0.45058174215400604
				],
				[
					7.209411006014302,
					-0.45058174215400604
				],
				[
					9.011772351813677,
					-1.3517624150536935
				],
				[
					11.264715439767134,
					-1.8023613457994132
				],
				[
					13.517658527720515,
					-2.7035248301074253
				],
				[
					16.22118335782798,
					-3.1541237608531065
				],
				[
					20.727069533734817,
					-4.505886175906839
				],
				[
					26.584735313287023,
					-6.308247521706251
				],
				[
					30.1894236277025,
					-6.758829263860258
				],
				[
					34.69530980360934,
					-8.110591678913952
				],
				[
					38.75061423736217,
					-8.110591678913952
				],
				[
					43.25650041326901,
					-9.011772351813677
				],
				[
					46.86122310486783,
					-9.912953024713364
				],
				[
					50.01532967712931,
					-9.912953024713364
				],
				[
					52.71885450723669,
					-9.912953024713364
				],
				[
					54.07063411088206,
					-9.912953024713364
				],
				[
					55.42241371452751,
					-10.363534766867371
				],
				[
					55.872995456681515,
					-10.363534766867371
				],
				[
					56.77415894098952,
					-10.81413369761309
				],
				[
					57.22474068314353,
					-10.81413369761309
				],
				[
					58.12593854463489,
					-10.81413369761309
				],
				[
					58.5765202867889,
					-10.81413369761309
				],
				[
					59.47768377109699,
					-10.81413369761309
				],
				[
					59.928299890434346,
					-10.81413369761309
				],
				[
					59.928299890434346,
					-10.81413369761309
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 924,
			"versionNonce": 1135620541,
			"isDeleted": false,
			"id": "tEiQifwDtyxtZiFqCaazq",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -161.21479958875895,
			"y": 400.6488201986145,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 59.92826551325092,
			"height": 6.308230333114576,
			"seed": 374366504,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.9011634843080121,
					0
				],
				[
					-1.351745226462018,
					0
				],
				[
					-0.45058174215400604,
					0
				],
				[
					0.9011978614913629,
					0
				],
				[
					2.7035248301074635,
					0.45058174215400604
				],
				[
					4.505886175906839,
					0.45058174215400604
				],
				[
					7.209411006014302,
					0.45058174215400604
				],
				[
					9.912970213305039,
					0.45058174215400604
				],
				[
					14.869438131365884,
					0.45058174215400604
				],
				[
					19.375324307272724,
					0
				],
				[
					23.88121048317956,
					-0.4505989307457197
				],
				[
					28.3870966590864,
					-1.3517624150537317
				],
				[
					32.44240109283923,
					-2.2529430879534194
				],
				[
					36.94828726874607,
					-3.154123760853145
				],
				[
					41.45417344465291,
					-3.154123760853145
				],
				[
					45.058861759068385,
					-4.505886175906839
				],
				[
					48.66358445066721,
					-4.505886175906839
				],
				[
					51.81769102292868,
					-4.956485106652558
				],
				[
					54.52121585303607,
					-4.956485106652558
				],
				[
					55.87299545668144,
					-5.8576485909605704
				],
				[
					56.77415894098952,
					-5.8576485909605704
				],
				[
					57.224775060326884,
					-5.8576485909605704
				],
				[
					57.675356802480884,
					-5.8576485909605704
				],
				[
					58.5765202867889,
					-5.8576485909605704
				],
				[
					58.5765202867889,
					-5.8576485909605704
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 937,
			"versionNonce": 871535763,
			"isDeleted": false,
			"id": "NqHcRvIDGTN6OZ6yXs7OG",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -167.97362885261913,
			"y": 431.7394416878083,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 69.39065398440195,
			"height": 8.110574490322314,
			"seed": 1123679272,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					3.1541409494447437,
					0.9011634843080503
				],
				[
					3.60472269159875,
					0.9011634843080503
				],
				[
					4.956467918060844,
					0.9011634843080503
				],
				[
					6.758829263860219,
					0.9011634843080503
				],
				[
					9.462354093967683,
					0.4505817421540443
				],
				[
					12.16591330125842,
					0
				],
				[
					17.572962961473273,
					-0.9011978614913629
				],
				[
					22.9800126216882,
					-1.802361345799375
				],
				[
					27.485898797595038,
					-2.2529430879534194
				],
				[
					32.89298283499324,
					-3.1541409494447823
				],
				[
					36.04708940725471,
					-3.1541409494447823
				],
				[
					40.55297558316155,
					-4.055304433752794
				],
				[
					44.15769827476029,
					-4.505886175906839
				],
				[
					46.86122310486776,
					-4.505886175906839
				],
				[
					49.11416619282114,
					-4.505886175906839
				],
				[
					51.3671092807746,
					-4.505886175906839
				],
				[
					53.169470626573975,
					-4.505886175906839
				],
				[
					53.620052368727976,
					-4.505886175906839
				],
				[
					54.97183197237342,
					-4.505886175906839
				],
				[
					56.323577198835444,
					-4.505886175906839
				],
				[
					57.67535680248081,
					-4.505886175906839
				],
				[
					58.12593854463482,
					-4.505886175906839
				],
				[
					59.47771814828026,
					-5.407084037398201
				],
				[
					60.378881632588275,
					-5.407084037398201
				],
				[
					60.82946337474228,
					-5.407084037398201
				],
				[
					61.730661236233644,
					-5.407084037398201
				],
				[
					62.18124297838765,
					-5.407084037398201
				],
				[
					62.63182472054166,
					-5.857665779552208
				],
				[
					63.9836043241871,
					-5.857665779552208
				],
				[
					64.88476780849511,
					-5.857665779552208
				],
				[
					65.33534955064911,
					-5.857665779552208
				],
				[
					65.78593129280313,
					-6.758829263860258
				],
				[
					66.68712915429448,
					-6.758829263860258
				],
				[
					67.1377108964485,
					-7.209411006014264
				],
				[
					68.03887438075658,
					-7.209411006014264
				],
				[
					68.48949050009394,
					-7.209411006014264
				],
				[
					69.39065398440195,
					-7.209411006014264
				],
				[
					69.39065398440195,
					-7.209411006014264
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 924,
			"versionNonce": 698151453,
			"isDeleted": false,
			"id": "cufx4BGqWKQbCyN1NJMQL",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -159.41243824295958,
			"y": 450.6641498757437,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 58.12593854463489,
			"height": 7.209411006014264,
			"seed": 2109224744,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.45058174215408253,
					0
				],
				[
					1.3517796036454455,
					0.45058174215400604
				],
				[
					2.7035248301074635,
					0.45058174215400604
				],
				[
					3.6047226915988264,
					1.3517796036453689
				],
				[
					4.956467918060921,
					1.3517796036453689
				],
				[
					6.758829263860296,
					1.3517796036453689
				],
				[
					9.011772351813677,
					1.3517796036453689
				],
				[
					11.715297181921141,
					1.3517796036453689
				],
				[
					15.770601615673973,
					0.9011978614913629
				],
				[
					20.276487791580813,
					0
				],
				[
					25.68353745179566,
					-0.9011634843080503
				],
				[
					31.54120323134787,
					-2.2529430879534194
				],
				[
					36.948252891562795,
					-3.1541065722614694
				],
				[
					42.355336928960995,
					-4.055304433752832
				],
				[
					46.86122310486783,
					-4.055304433752832
				],
				[
					50.46591141928331,
					-4.505886175906839
				],
				[
					53.169470626574046,
					-4.505886175906839
				],
				[
					54.07063411088206,
					-4.505886175906839
				],
				[
					54.97179759519015,
					-5.407049660214889
				],
				[
					55.42241371452751,
					-5.407049660214889
				],
				[
					56.323577198835515,
					-5.857631402368895
				],
				[
					56.77415894098952,
					-5.857631402368895
				],
				[
					57.675356802480884,
					-5.857631402368895
				],
				[
					58.12593854463489,
					-5.857631402368895
				],
				[
					58.12593854463489,
					-5.857631402368895
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 919,
			"versionNonce": 7899699,
			"isDeleted": false,
			"id": "JfncaBQazY1s4ohjfmiiH",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -160.76421784660494,
			"y": 477.69946693118465,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 69.84123572655604,
			"height": 1.3517452264620564,
			"seed": 1526141480,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					2.2529430879534575,
					0
				],
				[
					3.6047226915988264,
					0
				],
				[
					6.30824752170629,
					0
				],
				[
					9.011772351813677,
					0
				],
				[
					13.06707678556651,
					0
				],
				[
					18.47416082296471,
					0
				],
				[
					23.88121048317956,
					0
				],
				[
					29.28826014339449,
					-0.4505817421540443
				],
				[
					35.5965076651007,
					-0.4505817421540443
				],
				[
					41.904755186806916,
					-1.3517452264620564
				],
				[
					49.114166192821216,
					-1.3517452264620564
				],
				[
					55.42241371452743,
					-1.3517452264620564
				],
				[
					60.37888163258835,
					-1.3517452264620564
				],
				[
					63.9836043241871,
					-1.3517452264620564
				],
				[
					66.68712915429457,
					-1.3517452264620564
				],
				[
					68.03890875793994,
					-1.3517452264620564
				],
				[
					68.48949050009394,
					-1.3517452264620564
				],
				[
					69.39065398440202,
					-1.3517452264620564
				],
				[
					69.84123572655604,
					-1.3517452264620564
				],
				[
					69.84123572655604,
					-1.3517452264620564
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 920,
			"versionNonce": 1221764733,
			"isDeleted": false,
			"id": "K6YDk6U-l9pzjk-5Pm8Re",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -149.95008414899183,
			"y": 503.83362050231773,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 31.090621489193786,
			"height": 5.407084037398201,
			"seed": 27430184,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					3.1541409494447437,
					0
				],
				[
					4.505886175906839,
					0
				],
				[
					6.758829263860219,
					0
				],
				[
					9.462354093967683,
					-0.9011978614913629
				],
				[
					11.264715439767057,
					-0.9011978614913629
				],
				[
					13.96824026987452,
					-1.3517796036453689
				],
				[
					15.770601615673897,
					-2.2529430879534194
				],
				[
					18.47412644578136,
					-2.7035248301074253
				],
				[
					20.276487791580735,
					-2.7035248301074253
				],
				[
					22.07884913738011,
					-3.604722691598788
				],
				[
					24.33179222533357,
					-4.055304433752832
				],
				[
					25.23295570964158,
					-4.055304433752832
				],
				[
					26.58473531328695,
					-4.956467918060844
				],
				[
					27.485898797595038,
					-5.407084037398201
				],
				[
					27.936514916932392,
					-5.407084037398201
				],
				[
					28.837678401240407,
					-5.407084037398201
				],
				[
					29.28826014339441,
					-5.407084037398201
				],
				[
					29.738841885548418,
					-5.407084037398201
				],
				[
					30.64003974703978,
					-5.407084037398201
				],
				[
					31.090621489193786,
					-5.407084037398201
				],
				[
					31.090621489193786,
					-5.407084037398201
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 1013,
			"versionNonce": 1609485267,
			"isDeleted": false,
			"id": "ufq-UNN3r_krgrW7rC_dm",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -49.919424794733374,
			"y": 345.6770054148327,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 4.956502295244196,
			"height": 159.5083603139471,
			"seed": 1529260072,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.45058174215400604
				],
				[
					0,
					1.8023613457994132
				],
				[
					0,
					2.2529430879534194
				],
				[
					0,
					3.604705503007151
				],
				[
					0,
					4.956467918060844
				],
				[
					0,
					6.758829263860258
				],
				[
					0,
					8.11059167891399
				],
				[
					0,
					9.912953024713403
				],
				[
					0,
					11.715297181921102
				],
				[
					0,
					13.96824026987452
				],
				[
					0,
					15.320019873519929
				],
				[
					-0.4505473649706553,
					17.122364030727667
				],
				[
					-1.351710849278744,
					18.92472537652708
				],
				[
					-1.351710849278744,
					20.727069533734777
				],
				[
					-1.351710849278744,
					22.078849137380185
				],
				[
					-1.351710849278744,
					23.881193294587924
				],
				[
					-1.351710849278744,
					25.23295570964162
				],
				[
					-1.351710849278744,
					26.134136382541342
				],
				[
					-1.351710849278744,
					27.485898797595038
				],
				[
					-1.351710849278744,
					28.38707947049476
				],
				[
					-1.351710849278744,
					29.738841885548457
				],
				[
					-1.351710849278744,
					30.64002255844818
				],
				[
					-1.351710849278744,
					31.090621489193865
				],
				[
					-1.802326968616101,
					31.991784973501876
				],
				[
					-1.802326968616101,
					32.44238390424759
				],
				[
					-1.802326968616101,
					33.79414631930129
				],
				[
					-1.802326968616101,
					34.24472806145529
				],
				[
					-1.802326968616101,
					36.04708940725471
				],
				[
					-1.802326968616101,
					37.39885182230844
				],
				[
					-1.802326968616101,
					39.651794910261856
				],
				[
					-2.7034904529241133,
					41.454156256061275
				],
				[
					-2.7034904529241133,
					44.157681086168694
				],
				[
					-2.7034904529241133,
					45.058861759068385
				],
				[
					-2.7034904529241133,
					47.311804847021804
				],
				[
					-2.7034904529241133,
					48.21298551992153
				],
				[
					-3.15410657226147,
					50.46592860787495
				],
				[
					-3.15410657226147,
					52.26827276508265
				],
				[
					-3.604653937232125,
					54.07063411088206
				],
				[
					-3.604653937232125,
					56.77415894098949
				],
				[
					-3.604653937232125,
					58.5765202867889
				],
				[
					-3.604653937232125,
					60.82946337474232
				],
				[
					-3.604653937232125,
					62.63180753195006
				],
				[
					-4.50588617590684,
					65.33536673924084
				],
				[
					-4.50588617590684,
					67.1376937078569
				],
				[
					-4.50588617590684,
					68.48947331150231
				],
				[
					-4.50588617590684,
					69.84125291514768
				],
				[
					-4.50588617590684,
					71.19299814160972
				],
				[
					-4.50588617590684,
					71.64357988376373
				],
				[
					-4.50588617590684,
					72.99535948740915
				],
				[
					-4.50588617590684,
					74.34713909105452
				],
				[
					-4.50588617590684,
					74.79772083320852
				],
				[
					-4.50588617590684,
					76.14946605967057
				],
				[
					-4.50588617590684,
					77.50124566331598
				],
				[
					-4.50588617590684,
					78.85302526696135
				],
				[
					-4.50588617590684,
					80.20477049342341
				],
				[
					-4.50588617590684,
					81.10596835491476
				],
				[
					-4.50588617590684,
					82.45771358137682
				],
				[
					-4.50588617590684,
					84.26007492717623
				],
				[
					-4.50588617590684,
					86.51301801512966
				],
				[
					-4.50588617590684,
					87.86479761877503
				],
				[
					-4.50588617590684,
					89.66712458739109
				],
				[
					-4.50588617590684,
					91.4694859331905
				],
				[
					-4.50588617590684,
					92.82126553683587
				],
				[
					-4.50588617590684,
					94.62362688263528
				],
				[
					-4.50588617590684,
					96.8765699705887
				],
				[
					-4.50588617590684,
					98.67889693920476
				],
				[
					-4.50588617590684,
					100.48125828500417
				],
				[
					-4.50588617590684,
					104.08598097660297
				],
				[
					-4.50588617590684,
					106.7895058067104
				],
				[
					-4.055270056569483,
					109.49303063681785
				],
				[
					-4.055270056569483,
					111.29539198261723
				],
				[
					-3.604653937232125,
					113.99891681272469
				],
				[
					-3.604653937232125,
					115.80127815852407
				],
				[
					-3.604653937232125,
					117.60363950432348
				],
				[
					-3.604653937232125,
					118.95538473078554
				],
				[
					-2.7034904529241133,
					120.30716433443091
				],
				[
					-2.7034904529241133,
					121.65894393807632
				],
				[
					-2.7034904529241133,
					123.01068916453838
				],
				[
					-2.7034904529241133,
					124.36246876818375
				],
				[
					-2.7034904529241133,
					124.81305051033775
				],
				[
					-2.7034904529241133,
					125.26363225249179
				],
				[
					-2.7034904529241133,
					126.16483011398316
				],
				[
					-2.7034904529241133,
					126.61541185613716
				],
				[
					-2.7034904529241133,
					127.51657534044521
				],
				[
					-2.7034904529241133,
					127.96715708259921
				],
				[
					-2.7034904529241133,
					128.41777320193657
				],
				[
					-2.7034904529241133,
					129.76951842839864
				],
				[
					-2.252943087953458,
					131.121298032044
				],
				[
					-2.252943087953458,
					132.47304325850607
				],
				[
					-2.252943087953458,
					133.82482286215142
				],
				[
					-2.252943087953458,
					135.17660246579683
				],
				[
					-1.351710849278744,
					136.9789294344129
				],
				[
					-1.351710849278744,
					138.33070903805827
				],
				[
					-1.351710849278744,
					140.13307038385767
				],
				[
					-0.9011634843080122,
					141.48481561031974
				],
				[
					-0.9011634843080122,
					143.28717695611914
				],
				[
					-0.9011634843080122,
					144.63895655976452
				],
				[
					-0.4505473649706553,
					146.44131790556392
				],
				[
					-0.4505473649706553,
					147.793063132026
				],
				[
					-0.4505473649706553,
					149.59542447782536
				],
				[
					-0.4505473649706553,
					150.94720408147077
				],
				[
					0.45061611933735696,
					152.29894930793282
				],
				[
					0.45061611933735696,
					153.6507289115782
				],
				[
					0.45061611933735696,
					155.00247413804024
				],
				[
					0.45061611933735696,
					156.35425374168562
				],
				[
					0.45061611933735696,
					156.80483548383967
				],
				[
					0.45061611933735696,
					157.25541722599365
				],
				[
					0.45061611933735696,
					158.15661508748502
				],
				[
					0.45061611933735696,
					158.60719682963904
				],
				[
					0.45061611933735696,
					159.5083603139471
				],
				[
					0,
					159.5083603139471
				],
				[
					-0.4505473649706553,
					159.5083603139471
				],
				[
					-0.9011634843080122,
					159.05777857179308
				],
				[
					-0.9011634843080122,
					159.05777857179308
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 930,
			"versionNonce": 1947389661,
			"isDeleted": false,
			"id": "OVTV-1mHaEYOg0_jsuCCS",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -54.87585833561084,
			"y": 496.6242094963034,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 14.869438131365884,
			"height": 10.363517578275733,
			"seed": 1131373352,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.9011634843080121,
					0
				],
				[
					1.3517796036453689,
					0
				],
				[
					2.252943087953381,
					0
				],
				[
					2.252943087953381,
					0.9011634843080121
				],
				[
					2.703490452924036,
					1.3517452264620564
				],
				[
					2.703490452924036,
					2.2529430879534194
				],
				[
					3.60472269159875,
					3.154106572261431
				],
				[
					3.60472269159875,
					4.055270056569482
				],
				[
					3.60472269159875,
					4.505886175906839
				],
				[
					4.055270056569482,
					5.857631402368895
				],
				[
					4.505886175906839,
					7.209411006014264
				],
				[
					4.505886175906839,
					8.56115623247632
				],
				[
					5.407049660214851,
					9.011772351813677
				],
				[
					5.407049660214851,
					9.912935836121688
				],
				[
					5.407049660214851,
					10.363517578275733
				],
				[
					5.857665779552208,
					10.363517578275733
				],
				[
					6.758829263860219,
					10.363517578275733
				],
				[
					7.209376628830874,
					10.363517578275733
				],
				[
					8.110608867505588,
					10.363517578275733
				],
				[
					9.912935836121688,
					7.6599927481682695
				],
				[
					10.363551955459046,
					6.308213144522901
				],
				[
					11.715262804737714,
					4.956467918060844
				],
				[
					12.616495043412426,
					3.6046883144154758
				],
				[
					13.517658527720515,
					2.2529430879534194
				],
				[
					13.517658527720515,
					1.8023269686160623
				],
				[
					14.418822012028528,
					1.8023269686160623
				],
				[
					14.418822012028528,
					0.9011634843080121
				],
				[
					14.869438131365884,
					0.45058174215400604
				],
				[
					14.869438131365884,
					1.3517452264620564
				],
				[
					14.869438131365884,
					1.8023269686160623
				],
				[
					14.869438131365884,
					1.8023269686160623
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 1098,
			"versionNonce": 644602227,
			"isDeleted": false,
			"id": "DvRSyD1U",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 1.5944815347316315,
			"x": -126.67162410986745,
			"y": 418.8996815448725,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 154.31272888183594,
			"height": 13.730713953716666,
			"seed": 954777128,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 10.984571162973333,
			"fontFamily": 1,
			"text": "order of removal from stack",
			"rawText": "order of removal from stack",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "order of removal from stack",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 983,
			"versionNonce": 703523645,
			"isDeleted": false,
			"id": "GXSzCzQcWFbIZ9A00Zai7",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -213.03249061168754,
			"y": 509.69128628186996,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 8.56119060965967,
			"height": 155.9036719995316,
			"seed": 209631528,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.9011978614913629
				],
				[
					0,
					-1.3517796036453689
				],
				[
					0,
					-1.802361345799375
				],
				[
					0,
					-2.703559207290814
				],
				[
					0,
					-3.1541409494448205
				],
				[
					0,
					-4.055304433752832
				],
				[
					0,
					-4.505886175906839
				],
				[
					0,
					-4.956502295244196
				],
				[
					0.45058174215400604,
					-5.857665779552246
				],
				[
					0.45058174215400604,
					-6.308247521706251
				],
				[
					0.9011978614913629,
					-7.209445383197615
				],
				[
					0.9011978614913629,
					-8.56119060965967
				],
				[
					1.802361345799375,
					-9.462388471151034
				],
				[
					1.802361345799375,
					-10.363551955459084
				],
				[
					1.802361345799375,
					-10.81413369761309
				],
				[
					1.802361345799375,
					-12.16591330125846
				],
				[
					2.252943087953381,
					-13.06707678556651
				],
				[
					2.252943087953381,
					-13.517658527720515
				],
				[
					2.252943087953381,
					-14.869438131365923
				],
				[
					2.252943087953381,
					-16.22121773501129
				],
				[
					2.252943087953381,
					-18.023544703627355
				],
				[
					2.252943087953381,
					-19.37532430727276
				],
				[
					2.252943087953381,
					-20.727103910918128
				],
				[
					2.252943087953381,
					-21.62826739522618
				],
				[
					2.252943087953381,
					-22.529430879534193
				],
				[
					2.252943087953381,
					-23.8812104831796
				],
				[
					2.252943087953381,
					-25.23299008682497
				],
				[
					2.252943087953381,
					-25.683571828978973
				],
				[
					2.252943087953381,
					-27.03531705544103
				],
				[
					2.252943087953381,
					-28.38709665908644
				],
				[
					2.252943087953381,
					-28.837678401240442
				],
				[
					2.252943087953381,
					-30.189458004885815
				],
				[
					2.252943087953381,
					-30.640039747039857
				],
				[
					2.252943087953381,
					-31.54120323134787
				],
				[
					2.252943087953381,
					-32.892982834993276
				],
				[
					2.252943087953381,
					-33.79414631930129
				],
				[
					2.252943087953381,
					-34.69534418079265
				],
				[
					2.252943087953381,
					-35.145925922946695
				],
				[
					2.252943087953381,
					-36.04708940725471
				],
				[
					2.252943087953381,
					-37.398869010900114
				],
				[
					2.252943087953381,
					-38.30003249520813
				],
				[
					2.252943087953381,
					-39.65181209885353
				],
				[
					2.252943087953381,
					-40.55297558316155
				],
				[
					2.252943087953381,
					-41.90475518680695
				],
				[
					1.3517796036453689,
					-42.805918671114966
				],
				[
					1.3517796036453689,
					-44.15769827476037
				],
				[
					0.9011978614913629,
					-45.50947787840574
				],
				[
					0.45058174215400604,
					-46.8612231048678
				],
				[
					0.45058174215400604,
					-48.213002708513166
				],
				[
					-0.45058174215408253,
					-49.56474793497522
				],
				[
					-0.9011634843080886,
					-50.465945796466585
				],
				[
					-0.9011634843080886,
					-51.81769102292864
				],
				[
					-0.9011634843080886,
					-52.718888884420004
				],
				[
					-0.9011634843080886,
					-54.521250230219415
				],
				[
					-0.9011634843080886,
					-54.97183197237342
				],
				[
					-0.9011634843080886,
					-56.32357719883548
				],
				[
					-0.9011634843080886,
					-57.675356802480884
				],
				[
					-0.9011634843080886,
					-59.02713640612625
				],
				[
					-0.9011634843080886,
					-60.37888163258831
				],
				[
					-0.9011634843080886,
					-61.73066123623368
				],
				[
					-0.9011634843080886,
					-62.63182472054173
				],
				[
					-0.9011634843080886,
					-63.9836043241871
				],
				[
					0,
					-65.33534955064916
				],
				[
					0,
					-66.68712915429452
				],
				[
					0,
					-68.03890875793994
				],
				[
					0,
					-68.48949050009394
				],
				[
					0,
					-69.390653984402
				],
				[
					0,
					-69.841235726556
				],
				[
					0,
					-71.19301533020136
				],
				[
					0,
					-71.6435970723554
				],
				[
					0,
					-72.99537667600077
				],
				[
					0,
					-73.89654016030883
				],
				[
					0.45058174215400604,
					-75.2483197639542
				],
				[
					0.45058174215400604,
					-75.6989015061082
				],
				[
					0.45058174215400604,
					-77.05068110975361
				],
				[
					0.45058174215400604,
					-77.50126285190761
				],
				[
					0.9011978614913629,
					-78.85300807836967
				],
				[
					0.9011978614913629,
					-79.30362419770702
				],
				[
					0.9011978614913629,
					-80.65536942416908
				],
				[
					0.9011978614913629,
					-82.00714902781445
				],
				[
					0.9011978614913629,
					-83.3588942542765
				],
				[
					0.9011978614913629,
					-85.16125560007592
				],
				[
					0.9011978614913629,
					-87.41419868802934
				],
				[
					0.9011978614913629,
					-88.31539654952071
				],
				[
					0.9011978614913629,
					-90.56833963747412
				],
				[
					0.9011978614913629,
					-91.46950312178214
				],
				[
					0.9011978614913629,
					-93.72244620973555
				],
				[
					0.9011978614913629,
					-95.52480755553498
				],
				[
					0.9011978614913629,
					-98.22833238564239
				],
				[
					0.9011978614913629,
					-100.03069373144181
				],
				[
					0.9011978614913629,
					-102.73421856154923
				],
				[
					0.9011978614913629,
					-104.53657990734865
				],
				[
					0.9011978614913629,
					-106.33892406455638
				],
				[
					0.9011978614913629,
					-108.5918671525098
				],
				[
					0.9011978614913629,
					-110.39422849830922
				],
				[
					0.9011978614913629,
					-111.74599091336292
				],
				[
					0.9011978614913629,
					-113.54835225916233
				],
				[
					0.9011978614913629,
					-115.35069641637006
				],
				[
					0.9011978614913629,
					-116.70247602001547
				],
				[
					0.9011978614913629,
					-118.05423843506917
				],
				[
					0.9011978614913629,
					-119.8565825922769
				],
				[
					0.9011978614913629,
					-121.2083621959223
				],
				[
					0.9011978614913629,
					-122.560124610976
				],
				[
					1.802361345799375,
					-123.01070635313
				],
				[
					1.802361345799375,
					-124.36246876818375
				],
				[
					2.252943087953381,
					-125.26364944108343
				],
				[
					2.252943087953381,
					-125.71424837182914
				],
				[
					2.252943087953381,
					-126.16483011398316
				],
				[
					2.252943087953381,
					-127.06601078688284
				],
				[
					3.1541409494447437,
					-127.51659252903684
				],
				[
					3.1541409494447437,
					-128.41777320193657
				],
				[
					3.1541409494447437,
					-128.86835494409058
				],
				[
					3.60472269159875,
					-128.86835494409058
				],
				[
					3.60472269159875,
					-129.76953561699025
				],
				[
					3.60472269159875,
					-130.220134547736
				],
				[
					4.055304433752756,
					-130.220134547736
				],
				[
					4.055304433752756,
					-130.67071628988998
				],
				[
					4.055304433752756,
					-131.57189696278968
				],
				[
					4.055304433752756,
					-132.0224787049437
				],
				[
					4.055304433752756,
					-132.92365937784342
				],
				[
					4.055304433752756,
					-133.3742411199974
				],
				[
					4.055304433752756,
					-134.2754217928971
				],
				[
					4.055304433752756,
					-134.72602072364282
				],
				[
					4.055304433752756,
					-136.0777831386965
				],
				[
					4.055304433752756,
					-137.42954555375024
				],
				[
					4.055304433752756,
					-138.33072622664994
				],
				[
					4.055304433752756,
					-139.68248864170366
				],
				[
					4.055304433752756,
					-141.03425105675737
				],
				[
					4.055304433752756,
					-141.9354317296571
				],
				[
					4.956467918060844,
					-143.7377930754565
				],
				[
					4.956467918060844,
					-145.08955549051018
				],
				[
					4.956467918060844,
					-145.5401372326642
				],
				[
					5.407084037398201,
					-146.89189964771793
				],
				[
					5.407084037398201,
					-147.34249857846362
				],
				[
					5.407084037398201,
					-148.24367925136335
				],
				[
					6.308247521706213,
					-148.69426099351733
				],
				[
					6.308247521706213,
					-150.04602340857105
				],
				[
					6.308247521706213,
					-150.94720408147077
				],
				[
					6.758829263860219,
					-151.39778582362476
				],
				[
					6.758829263860219,
					-152.74956542727017
				],
				[
					6.758829263860219,
					-153.20014716942418
				],
				[
					6.758829263860219,
					-154.10132784232388
				],
				[
					6.758829263860219,
					-154.55190958447787
				],
				[
					6.758829263860219,
					-155.00250851522358
				],
				[
					7.660027125351582,
					-155.00250851522358
				],
				[
					7.660027125351582,
					-155.9036719995316
				],
				[
					7.660027125351582,
					-155.4530902573776
				],
				[
					7.660027125351582,
					-155.4530902573776
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 886,
			"versionNonce": 1630941971,
			"isDeleted": false,
			"id": "sNWQQVwkVw-CAcUiG4A1a",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -204.921881744182,
			"y": 355.5899584395461,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 12.616495043412426,
			"height": 11.264715439767096,
			"seed": 295523368,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.9011978614913629,
					0
				],
				[
					-1.3517796036453689,
					0
				],
				[
					-2.252943087953381,
					0
				],
				[
					-2.703524830107387,
					0.45059893074568147
				],
				[
					-2.703524830107387,
					0.9011806728996875
				],
				[
					-3.60472269159875,
					1.8023613457994132
				],
				[
					-4.055304433752832,
					2.2529430879534194
				],
				[
					-4.505886175906839,
					2.7035420186991006
				],
				[
					-5.407084037398201,
					2.7035420186991006
				],
				[
					-5.407084037398201,
					3.604705503007113
				],
				[
					-5.857665779552208,
					4.055304433752832
				],
				[
					-6.758829263860219,
					4.9564851066525195
				],
				[
					-6.758829263860219,
					5.407066848806526
				],
				[
					-7.209411006014226,
					5.407066848806526
				],
				[
					-7.209411006014226,
					6.308247521706251
				],
				[
					-7.660027125351582,
					6.308247521706251
				],
				[
					-7.660027125351582,
					6.758829263860258
				],
				[
					-7.209411006014226,
					6.758829263860258
				],
				[
					-6.308247521706213,
					5.857648590960532
				],
				[
					-6.308247521706213,
					5.407066848806526
				],
				[
					-5.857665779552208,
					5.407066848806526
				],
				[
					-5.857665779552208,
					4.505886175906839
				],
				[
					-4.956467918060844,
					4.055304433752832
				],
				[
					-4.505886175906839,
					4.055304433752832
				],
				[
					-4.505886175906839,
					3.1541237608531065
				],
				[
					-4.055304433752832,
					2.7035420186991006
				],
				[
					-3.1541409494447437,
					2.7035420186991006
				],
				[
					-3.1541409494447437,
					2.2529430879534194
				],
				[
					-2.703524830107387,
					1.3517624150536935
				],
				[
					-1.802361345799375,
					1.3517624150536935
				],
				[
					-1.802361345799375,
					0.9011806728996875
				],
				[
					-1.3517796036453689,
					0.9011806728996875
				],
				[
					-0.45058174215400604,
					0.9011806728996875
				],
				[
					0,
					0.9011806728996875
				],
				[
					0.45058174215400604,
					1.8023613457994132
				],
				[
					0.45058174215400604,
					2.2529430879534194
				],
				[
					1.3517452264620946,
					2.7035420186991006
				],
				[
					1.3517452264620946,
					3.604705503007113
				],
				[
					1.8023613457994514,
					4.055304433752832
				],
				[
					1.8023613457994514,
					4.9564851066525195
				],
				[
					2.7035248301074635,
					5.407066848806526
				],
				[
					2.7035248301074635,
					6.308247521706251
				],
				[
					3.1541065722614694,
					6.758829263860258
				],
				[
					3.1541065722614694,
					7.209428194605939
				],
				[
					3.1541065722614694,
					8.110591678913952
				],
				[
					4.055304433752832,
					8.56119060965967
				],
				[
					4.055304433752832,
					9.462371282559358
				],
				[
					4.505886175906839,
					9.462371282559358
				],
				[
					4.505886175906839,
					9.912953024713364
				],
				[
					4.505886175906839,
					10.81413369761309
				],
				[
					4.956467918060844,
					10.81413369761309
				],
				[
					4.956467918060844,
					11.264715439767096
				],
				[
					4.956467918060844,
					11.264715439767096
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 995,
			"versionNonce": 449346461,
			"isDeleted": false,
			"id": "yYl1xnVm",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 4.685211764148448,
			"x": -307.61289693732067,
			"y": 425.8817759082561,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 132.1326141357422,
			"height": 13.45817433623004,
			"seed": 1311805224,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 10.766539468984032,
			"fontFamily": 1,
			"text": "order of function calling ",
			"rawText": "order of function calling ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "order of function calling ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 955,
			"versionNonce": 818174131,
			"isDeleted": false,
			"id": "SqHwDiEr",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -237.0258579256538,
			"y": 300.2207526646375,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 150.11700439453125,
			"height": 23.551805088402567,
			"seed": 715418152,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 18.841444070722055,
			"fontFamily": 1,
			"text": "Stack Diagram :",
			"rawText": "Stack Diagram :",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Stack Diagram :",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 387,
			"versionNonce": 1859190781,
			"isDeleted": false,
			"id": "CeM1a88z",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -423.94474622316204,
			"y": 612.8613310103449,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 110.095947265625,
			"height": 20,
			"seed": 106021160,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "base condition",
			"rawText": "base condition",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "base condition",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 295,
			"versionNonce": 1656539731,
			"isDeleted": false,
			"id": "lLEqLc5VFjvJkpMpGdVUl",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -614.8256975328676,
			"y": 633.5646994356808,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 64.79157549825766,
			"height": 4.573511345277211,
			"seed": 593594200,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7622421983209051,
					-0.7622421983207914
				],
				[
					2.2867556726386056,
					-0.7622421983207914
				],
				[
					3.048997870959397,
					-0.7622421983207914
				],
				[
					4.573511345277211,
					-0.7622421983207914
				],
				[
					5.3357826212740065,
					-0.7622421983207914
				],
				[
					6.098024819594912,
					-0.7622421983207914
				],
				[
					7.622538293912726,
					-0.7622421983207914
				],
				[
					9.909293966551218,
					-0.7622421983207914
				],
				[
					10.671536164872123,
					-0.7622421983207914
				],
				[
					12.196049639189937,
					-0.7622421983207914
				],
				[
					12.958320915186732,
					-0.7622421983207914
				],
				[
					13.720563113507637,
					-0.7622421983207914
				],
				[
					15.245076587825338,
					-0.7622421983207914
				],
				[
					16.00731878614613,
					-0.7622421983207914
				],
				[
					17.531832260463943,
					-0.7622421983207914
				],
				[
					19.81858793310255,
					-0.7622421983207914
				],
				[
					20.580859209099458,
					-0.7622421983207914
				],
				[
					21.34310140742025,
					-2.2867265949626017
				],
				[
					22.86761488173795,
					-2.2867265949626017
				],
				[
					23.629857080058855,
					-3.049026948635401
				],
				[
					25.15437055437667,
					-3.049026948635401
				],
				[
					25.91661275269746,
					-3.049026948635401
				],
				[
					27.44112622701516,
					-3.049026948635401
				],
				[
					28.20339750301207,
					-3.049026948635401
				],
				[
					28.965639701332975,
					-3.049026948635401
				],
				[
					30.490153175650676,
					-3.049026948635401
				],
				[
					31.25239537397158,
					-3.049026948635401
				],
				[
					32.77690884828928,
					-3.049026948635401
				],
				[
					33.539151046610186,
					-3.049026948635401
				],
				[
					34.30142232260698,
					-3.049026948635401
				],
				[
					35.82593579692468,
					-3.049026948635401
				],
				[
					36.5881779952457,
					-3.049026948635401
				],
				[
					38.1126914695634,
					-3.049026948635401
				],
				[
					38.87493366788419,
					-3.049026948635401
				],
				[
					40.39944714220189,
					-3.049026948635401
				],
				[
					41.16168934052291,
					-3.049026948635401
				],
				[
					41.92396061651971,
					-3.049026948635401
				],
				[
					43.44847409083741,
					-3.049026948635401
				],
				[
					44.21071628915831,
					-3.049026948635401
				],
				[
					45.73522976347601,
					-3.049026948635401
				],
				[
					46.49747196179692,
					-3.049026948635401
				],
				[
					48.02198543611462,
					-3.049026948635401
				],
				[
					48.784227634435524,
					-3.049026948635401
				],
				[
					49.54649891043243,
					-3.049026948635401
				],
				[
					51.071012384750134,
					-3.049026948635401
				],
				[
					51.833254583070925,
					-3.049026948635401
				],
				[
					53.35776805738874,
					-3.049026948635401
				],
				[
					54.120010255709644,
					-3.049026948635401
				],
				[
					54.120010255709644,
					-4.573511345277211
				],
				[
					54.88228153170644,
					-4.573511345277211
				],
				[
					56.406765928348136,
					-4.573511345277211
				],
				[
					57.169037204345045,
					-4.573511345277211
				],
				[
					58.693550678662746,
					-4.573511345277211
				],
				[
					59.45579287698365,
					-4.573511345277211
				],
				[
					60.980306351301465,
					-4.573511345277211
				],
				[
					61.742548549622256,
					-4.573511345277211
				],
				[
					62.504819825619165,
					-4.573511345277211
				],
				[
					64.02930422226086,
					-4.573511345277211
				],
				[
					64.79157549825766,
					-4.573511345277211
				],
				[
					64.79157549825766,
					-4.573511345277211
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 375,
			"versionNonce": 1275721821,
			"isDeleted": false,
			"id": "d0RQ6NGVkn91iznf7X6se",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -531.740047575825,
			"y": 625.1799770987994,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 97.56848434654705,
			"height": 2.2867265949626017,
			"seed": 673725784,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					-1.524542551993818
				],
				[
					0.4978097250916385,
					-1.524542551993818
				],
				[
					1.493410185775717,
					-1.524542551993818
				],
				[
					1.9912009213680084,
					-1.524542551993818
				],
				[
					2.9868013820520125,
					-1.524542551993818
				],
				[
					3.4845921176443784,
					-1.524542551993818
				],
				[
					4.480192578328457,
					-1.524542551993818
				],
				[
					4.977983313920748,
					-1.524542551993818
				],
				[
					6.4713934996964655,
					-1.524542551993818
				],
				[
					7.964784695972836,
					-1.524542551993818
				],
				[
					9.955966627841496,
					-1.981915785129305
				],
				[
					11.947186538708927,
					-1.981915785129305
				],
				[
					14.933968931261667,
					-1.981915785129305
				],
				[
					16.42734113803869,
					-1.981915785129305
				],
				[
					18.418542059406697,
					-1.981915785129305
				],
				[
					20.40974298077478,
					-1.981915785129305
				],
				[
					22.400943902142863,
					-1.981915785129305
				],
				[
					23.894316108919885,
					-1.981915785129305
				],
				[
					25.387726294695604,
					-1.981915785129305
				],
				[
					26.38330776588026,
					-1.981915785129305
				],
				[
					26.881136480471284,
					-1.981915785129305
				],
				[
					27.378927216063648,
					-1.981915785129305
				],
				[
					28.374508687248344,
					-1.981915785129305
				],
				[
					28.872299422840673,
					-1.981915785129305
				],
				[
					29.867918873024024,
					-2.4392541255861517
				],
				[
					30.36570960861639,
					-2.4392541255861517
				],
				[
					31.361291079801084,
					-2.4392541255861517
				],
				[
					31.85911979439207,
					-2.4392541255861517
				],
				[
					32.35691052998443,
					-2.4392541255861517
				],
				[
					33.35249200116913,
					-2.4392541255861517
				],
				[
					34.84590218694481,
					-2.4392541255861517
				],
				[
					36.83710310831285,
					-3.353930806499573
				],
				[
					37.33489384390522,
					-3.353930806499573
				],
				[
					38.828266050682245,
					-3.353930806499573
				],
				[
					39.82388550086559,
					-3.8112691469564197
				],
				[
					40.32167623645796,
					-3.8112691469564197
				],
				[
					41.815086422233676,
					-3.8112691469564197
				],
				[
					42.31287715782601,
					-3.8112691469564197
				],
				[
					43.3084586290107,
					-3.8112691469564197
				],
				[
					43.806249364603026,
					-3.8112691469564197
				],
				[
					45.29965955037875,
					-3.8112691469564197
				],
				[
					45.797450285971074,
					-3.8112691469564197
				],
				[
					47.29086047174679,
					-3.8112691469564197
				],
				[
					49.779852128707205,
					-3.8112691469564197
				],
				[
					51.771053050075245,
					-3.8112691469564197
				],
				[
					53.76221599244464,
					-3.8112691469564197
				],
				[
					55.25562617822032,
					-3.8112691469564197
				],
				[
					57.2468270995884,
					-3.8112691469564197
				],
				[
					58.74019930636542,
					-3.8112691469564197
				],
				[
					60.73140022773343,
					-3.8112691469564197
				],
				[
					62.22481041350915,
					-3.8112691469564197
				],
				[
					63.71818262028617,
					-3.8112691469564197
				],
				[
					65.21159280606189,
					-3.8112691469564197
				],
				[
					65.70938354165425,
					-3.8112691469564197
				],
				[
					67.20279372742998,
					-3.8112691469564197
				],
				[
					68.19837519861463,
					-3.8112691469564197
				],
				[
					68.69616593420699,
					-3.8112691469564197
				],
				[
					69.19399464879798,
					-3.8112691469564197
				],
				[
					70.1895761199827,
					-3.8112691469564197
				],
				[
					70.68736685557508,
					-3.8112691469564197
				],
				[
					71.68298630575843,
					-3.8112691469564197
				],
				[
					72.18077704135072,
					-3.8112691469564197
				],
				[
					72.67856777694308,
					-3.8112691469564197
				],
				[
					73.67414924812782,
					-3.8112691469564197
				],
				[
					74.1719779627188,
					-3.8112691469564197
				],
				[
					75.16755943390346,
					-3.8112691469564197
				],
				[
					75.66535016949582,
					-3.8112691469564197
				],
				[
					76.66096961967918,
					-3.8112691469564197
				],
				[
					77.65655109086391,
					-3.8112691469564197
				],
				[
					79.14996127663954,
					-3.8112691469564197
				],
				[
					80.64333348341664,
					-3.8112691469564197
				],
				[
					81.6389529336,
					-3.8112691469564197
				],
				[
					82.13674366919228,
					-3.8112691469564197
				],
				[
					82.63453440478466,
					-3.8112691469564197
				],
				[
					83.63011587596938,
					-3.8112691469564197
				],
				[
					85.6213167973374,
					-3.8112691469564197
				],
				[
					86.11910753292976,
					-3.8112691469564197
				],
				[
					87.11472698311312,
					-3.8112691469564197
				],
				[
					87.61251771870548,
					-3.8112691469564197
				],
				[
					88.60809918989014,
					-3.8112691469564197
				],
				[
					89.10592790448119,
					-3.8112691469564197
				],
				[
					90.10150937566586,
					-3.8112691469564197
				],
				[
					90.59930011125822,
					-3.8112691469564197
				],
				[
					91.0970908468505,
					-3.8112691469564197
				],
				[
					92.09271029703393,
					-3.8112691469564197
				],
				[
					92.59050103262622,
					-3.8112691469564197
				],
				[
					93.58608250381096,
					-3.8112691469564197
				],
				[
					94.08391121840194,
					-3.8112691469564197
				],
				[
					95.07949268958667,
					-3.8112691469564197
				],
				[
					95.57728342517896,
					-3.8112691469564197
				],
				[
					96.07507416077134,
					-3.8112691469564197
				],
				[
					97.07069361095468,
					-3.8112691469564197
				],
				[
					97.56848434654705,
					-3.8112691469564197
				],
				[
					97.56848434654705,
					-3.8112691469564197
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 318,
			"versionNonce": 1274415091,
			"isDeleted": false,
			"id": "zksm4bYPG_6dHULVV8wyR",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -435.69604762591973,
			"y": 613.7460533472264,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 12.958291837510728,
			"height": 18.294103536460852,
			"seed": 200075352,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.5244843966418102,
					0
				],
				[
					2.2867265949626017,
					0
				],
				[
					3.048968793283507,
					1.5245425519935907
				],
				[
					4.573511345277211,
					1.5245425519935907
				],
				[
					4.573511345277211,
					2.2867847503146095
				],
				[
					5.335753543598116,
					2.2867847503146095
				],
				[
					5.335753543598116,
					3.049026948635401
				],
				[
					6.860237940239813,
					3.049026948635401
				],
				[
					6.860237940239813,
					4.573511345277211
				],
				[
					7.622538293912726,
					4.573511345277211
				],
				[
					7.622538293912726,
					5.33581169895001
				],
				[
					9.147022690554422,
					5.33581169895001
				],
				[
					9.147022690554422,
					6.860296095591821
				],
				[
					9.909264888875327,
					6.860296095591821
				],
				[
					9.909264888875327,
					7.622538293912612
				],
				[
					9.909264888875327,
					8.384780492233517
				],
				[
					10.671507087196233,
					8.384780492233517
				],
				[
					12.196049639189937,
					8.384780492233517
				],
				[
					12.958291837510728,
					8.384780492233517
				],
				[
					12.958291837510728,
					9.909323044227222
				],
				[
					11.433807440869032,
					10.671565242548013
				],
				[
					10.671507087196233,
					10.671565242548013
				],
				[
					9.909264888875327,
					10.671565242548013
				],
				[
					8.384780492233517,
					12.196049639189823
				],
				[
					7.622538293912726,
					12.958349992862622
				],
				[
					6.097995741919021,
					12.958349992862622
				],
				[
					5.335753543598116,
					14.482834389504433
				],
				[
					3.811269146956306,
					15.245076587825224
				],
				[
					3.048968793283507,
					15.245076587825224
				],
				[
					3.048968793283507,
					16.007318786146243
				],
				[
					2.2867265949626017,
					16.007318786146243
				],
				[
					2.2867265949626017,
					17.531861338139834
				],
				[
					0.7622421983209051,
					17.531861338139834
				],
				[
					0.7622421983209051,
					18.294103536460852
				],
				[
					0,
					18.294103536460852
				],
				[
					0,
					18.294103536460852
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 320,
			"versionNonce": 474277053,
			"isDeleted": false,
			"id": "kSCl5woevVZKVUD-HMYW7",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -536.3135589211022,
			"y": 718.1748628670412,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 99.09302689854076,
			"height": 16.769619139819042,
			"seed": 52943704,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7622421983207914,
					0
				],
				[
					2.286755672638492,
					0
				],
				[
					3.049026948635401,
					0
				],
				[
					4.573511345277211,
					0
				],
				[
					5.3357826212740065,
					0
				],
				[
					6.098024819594912,
					0
				],
				[
					7.622538293912612,
					1.524542551993818
				],
				[
					10.671565242548013,
					1.524542551993818
				],
				[
					12.958320915186732,
					1.524542551993818
				],
				[
					18.29410353646074,
					1.524542551993818
				],
				[
					22.105343605741155,
					1.524542551993818
				],
				[
					25.154370554376555,
					1.524542551993818
				],
				[
					32.014666649968376,
					1.524542551993818
				],
				[
					37.35042019356638,
					1.524542551993818
				],
				[
					45.73525884115196,
					1.524542551993818
				],
				[
					49.54652798810832,
					1.524542551993818
				],
				[
					56.406765928348136,
					1.524542551993818
				],
				[
					59.455792876983594,
					1.524542551993818
				],
				[
					64.79160457593366,
					1.524542551993818
				],
				[
					69.36511592121087,
					1.524542551993818
				],
				[
					70.88960031785263,
					1.524542551993818
				],
				[
					73.17638506816724,
					1.524542551993818
				],
				[
					73.93862726648808,
					1.524542551993818
				],
				[
					74.70086946480893,
					1.524542551993818
				],
				[
					76.2254120168027,
					1.524542551993818
				],
				[
					76.98765421512354,
					1.524542551993818
				],
				[
					78.5121386117653,
					1.524542551993818
				],
				[
					79.27438081008614,
					1.524542551993818
				],
				[
					80.036681163759,
					1.524542551993818
				],
				[
					81.56116556040075,
					1.524542551993818
				],
				[
					82.32340775872166,
					1.524542551993818
				],
				[
					83.84795031071536,
					1.524542551993818
				],
				[
					84.61019250903621,
					1.524542551993818
				],
				[
					86.13467690567796,
					1.524542551993818
				],
				[
					86.89691910399887,
					1.524542551993818
				],
				[
					87.65921945767167,
					1.524542551993818
				],
				[
					89.18370385431342,
					1.524542551993818
				],
				[
					89.94594605263433,
					1.524542551993818
				],
				[
					91.47048860462803,
					1.524542551993818
				],
				[
					92.23273080294894,
					0.7623003536729129
				],
				[
					93.75721519959063,
					0.7623003536729129
				],
				[
					94.51945739791154,
					0.7623003536729129
				],
				[
					95.28175775158434,
					0.7623003536729129
				],
				[
					96.80624214822615,
					0
				],
				[
					97.56848434654694,
					0
				],
				[
					96.04399994990524,
					-1.5244843966416965
				],
				[
					95.28175775158434,
					-1.5244843966416965
				],
				[
					94.51945739791154,
					-2.2867265949626017
				],
				[
					92.99497300126973,
					-2.2867265949626017
				],
				[
					92.23273080294894,
					-3.811269146956306
				],
				[
					90.70818825095523,
					-4.573511345277211
				],
				[
					89.94594605263433,
					-4.573511345277211
				],
				[
					89.94594605263433,
					-5.335753543598003
				],
				[
					88.42146165599252,
					-5.335753543598003
				],
				[
					87.65921945767167,
					-6.860237940239813
				],
				[
					86.89691910399887,
					-6.860237940239813
				],
				[
					86.89691910399887,
					-7.622538293912612
				],
				[
					85.37243470735712,
					-7.622538293912612
				],
				[
					86.13467690567796,
					-7.622538293912612
				],
				[
					86.89691910399887,
					-7.622538293912612
				],
				[
					87.65921945767167,
					-7.622538293912612
				],
				[
					89.18370385431342,
					-6.097995741918908
				],
				[
					89.94594605263433,
					-6.097995741918908
				],
				[
					91.47048860462803,
					-6.097995741918908
				],
				[
					92.23273080294894,
					-5.335753543598003
				],
				[
					93.75721519959063,
					-5.335753543598003
				],
				[
					94.51945739791154,
					-4.573511345277211
				],
				[
					95.28175775158434,
					-4.573511345277211
				],
				[
					95.28175775158434,
					-3.048968793283393
				],
				[
					96.80624214822615,
					-3.048968793283393
				],
				[
					97.56848434654694,
					-3.048968793283393
				],
				[
					97.56848434654694,
					-2.2867265949626017
				],
				[
					99.09302689854076,
					-2.2867265949626017
				],
				[
					98.33072654486784,
					-0.7622421983207914
				],
				[
					98.33072654486784,
					0
				],
				[
					97.56848434654694,
					1.524542551993818
				],
				[
					96.04399994990524,
					2.2867847503146095
				],
				[
					96.04399994990524,
					3.0490269486355146
				],
				[
					95.28175775158434,
					4.573569500629219
				],
				[
					95.28175775158434,
					5.335811698950124
				],
				[
					94.51945739791154,
					6.860296095591821
				],
				[
					92.99497300126973,
					7.622538293912726
				],
				[
					92.23273080294894,
					9.14708084590643
				],
				[
					90.70818825095523,
					9.14708084590643
				],
				[
					90.70818825095523,
					9.14708084590643
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 302,
			"versionNonce": 1651937683,
			"isDeleted": false,
			"id": "1z2c4tyd",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -435.3743267202781,
			"y": 705.9788713832032,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 104.06393432617188,
			"height": 20,
			"seed": 1606872616,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "recursive call",
			"rawText": "recursive call",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "recursive call",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 846,
			"versionNonce": 321078557,
			"isDeleted": false,
			"id": "QFwuJA2d",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -394.62319234706297,
			"y": 534.4719051585485,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 397.9518127441406,
			"height": 40,
			"seed": 1191380520,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# If you are calling a function again and again,\nyou can treat it as a separate call in the stack",
			"rawText": "# If you are calling a function again and again,\nyou can treat it as a separate call in the stack",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# If you are calling a function again and again,\nyou can treat it as a separate call in the stack",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 477,
			"versionNonce": 393537331,
			"isDeleted": false,
			"id": "1a7kixeI",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -329.7333355834754,
			"y": 583.2560164822795,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 370.1918640136719,
			"height": 40,
			"seed": 776371288,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# As u call a function again and again it will \ntake memory separately in Stack Memory",
			"rawText": "# As u call a function again and again it will \ntake memory separately in Stack Memory",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# As u call a function again and again it will \ntake memory separately in Stack Memory",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 608,
			"versionNonce": 1947638141,
			"isDeleted": false,
			"id": "jEBkCGx3",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -341.2614551145625,
			"y": 638.900511134631,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 373.663818359375,
			"height": 80,
			"seed": 34791768,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# No base condition -> Function calls will keep \nhappening, stack will be filled again and again \nand each function consumes some memory --->\n",
			"rawText": "# No base condition -> Function calls will keep \nhappening, stack will be filled again and again \nand each function consumes some memory --->\n",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# No base condition -> Function calls will keep \nhappening, stack will be filled again and again \nand each function consumes some memory --->\n",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 442,
			"versionNonce": 1901562067,
			"isDeleted": false,
			"id": "DhJgnLdf",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -274.41560646832,
			"y": 712.0767798920944,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 325.9197998046875,
			"height": 40,
			"seed": 461962792,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# Resulting in Stack over flow error,\ni.e. Memory limit of computer is exceeded.",
			"rawText": "# Resulting in Stack over flow error,\ni.e. Memory limit of computer is exceeded.",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# Resulting in Stack over flow error,\ni.e. Memory limit of computer is exceeded.",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1274,
			"versionNonce": 1915221587,
			"isDeleted": false,
			"id": "xhnGnJ3l-ejpDVoaOVk8z",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 200.2421321637338,
			"y": -372.656122887176,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 810.7795986610721,
			"height": 542.2523373967291,
			"seed": 1303538728,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421687811,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 1114,
			"versionNonce": 1706358387,
			"isDeleted": false,
			"id": "To6v9dZy",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 470.80646865670224,
			"y": -351.972221844981,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 202.07591247558594,
			"height": 35,
			"seed": 2011342632,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": " Why Recursion",
			"rawText": " Why Recursion",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": " Why Recursion",
			"lineHeight": 1.25
		},
		{
			"type": "ellipse",
			"version": 545,
			"versionNonce": 890379837,
			"isDeleted": false,
			"id": "Qigw1VvvRz8fuOYP0KF6q",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 898.6969951616823,
			"y": -358.0864618726871,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 80.9803541126721,
			"height": 85.47926267448713,
			"seed": 1674082904,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "mbEmtmf8"
				}
			],
			"updated": 1715421158212,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 469,
			"versionNonce": 1934864403,
			"isDeleted": false,
			"id": "mbEmtmf8",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 929.5222968680079,
			"y": -333.0683136794215,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 19.0679931640625,
			"height": 35,
			"seed": 1182232408,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "3",
			"rawText": "3",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Qigw1VvvRz8fuOYP0KF6q",
			"originalText": "3",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 808,
			"versionNonce": 1628262045,
			"isDeleted": false,
			"id": "tKSjNyXD",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 227.77324690049113,
			"y": -274.85011981534456,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 309.9837951660156,
			"height": 40,
			"seed": 886989864,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# It helps us in solving bigger/ complex\nproblems in a simple way.",
			"rawText": "# It helps us in solving bigger/ complex\nproblems in a simple way.",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# It helps us in solving bigger/ complex\nproblems in a simple way.",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1057,
			"versionNonce": 2083141043,
			"isDeleted": false,
			"id": "YSbyKERU",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 212.24599668658584,
			"y": -204.52724533577327,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 343.9998779296875,
			"height": 60,
			"seed": 1672360792,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# You can convert recursion solutions into \niteration and vice versa, once converted\niterations it becomes optimized ",
			"rawText": "# You can convert recursion solutions into \niteration and vice versa, once converted\niterations it becomes optimized ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# You can convert recursion solutions into \niteration and vice versa, once converted\niterations it becomes optimized ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1311,
			"versionNonce": 1526952701,
			"isDeleted": false,
			"id": "6yVoIW2g",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 211.08718104506943,
			"y": -106.97448525352456,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 365.1517333984375,
			"height": 60,
			"seed": 1330429528,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "-> It is also easier to solve complex problems\nusing recursion so it's a great first step in \nsolving a problem.... ",
			"rawText": "-> It is also easier to solve complex problems\nusing recursion so it's a great first step in \nsolving a problem.... ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "-> It is also easier to solve complex problems\nusing recursion so it's a great first step in \nsolving a problem.... ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1429,
			"versionNonce": 1600063315,
			"isDeleted": false,
			"id": "TxDuQZNE",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 201.42017724156926,
			"y": -7.694887421023509,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 390.9117736816406,
			"height": 40,
			"seed": 538319192,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "-> Space complexity : It is not constant because\nof recursive calls.",
			"rawText": "-> Space complexity : It is not constant because\nof recursive calls.",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "-> Space complexity : It is not constant because\nof recursive calls.",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1519,
			"versionNonce": 259394397,
			"isDeleted": false,
			"id": "79kOHO8n",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 248.027307165406,
			"y": 74.85544972599746,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 347.7437744140625,
			"height": 40,
			"seed": 1898296872,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "-> It helps in breaking down bigger problems \ninto smaller problems",
			"rawText": "-> It helps in breaking down bigger problems \ninto smaller problems",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "-> It helps in breaking down bigger problems \ninto smaller problems",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 751,
			"versionNonce": 1397269747,
			"isDeleted": false,
			"id": "yu1MDIC3",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 675.6396449547599,
			"y": -215.709904287629,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 294.13983154296875,
			"height": 35,
			"seed": 1627297112,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Visualizing Recursion :",
			"rawText": "Visualizing Recursion :",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Visualizing Recursion :",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 323,
			"versionNonce": 1589024701,
			"isDeleted": false,
			"id": "Atre6pNJR6Pjv2A-ufMYP",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 713.5810756903097,
			"y": -169.57164652969027,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 288.928651503787,
			"height": 314.38497233504006,
			"seed": 621910616,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 448,
			"versionNonce": 2137886355,
			"isDeleted": false,
			"id": "7HGTrOiH",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 767.7867493944516,
			"y": -125.47711649448479,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 51.823974609375,
			"height": 20,
			"seed": 1751769944,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "main ()",
			"rawText": "main ()",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "main ()",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 440,
			"versionNonce": 585537565,
			"isDeleted": false,
			"id": "RaD1usPH",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 764.8462122452449,
			"y": -82.97760556263205,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 59.16795349121094,
			"height": 20,
			"seed": 237924136,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "print (1)",
			"rawText": "print (1)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print (1)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 478,
			"versionNonce": 1451508787,
			"isDeleted": false,
			"id": "4XJ3Boq8",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 757.7354567728082,
			"y": -37.6415874434644,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 66.22395324707031,
			"height": 20,
			"seed": 116947800,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "print (2)",
			"rawText": "print (2)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print (2)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 423,
			"versionNonce": 1979157629,
			"isDeleted": false,
			"id": "SRdkoDIp",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 757.4547616834441,
			"y": 10.034785765081722,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 65.72795104980469,
			"height": 20,
			"seed": 168209752,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "print (3)",
			"rawText": "print (3)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print (3)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 418,
			"versionNonce": 812860883,
			"isDeleted": false,
			"id": "rOZzSNwb",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 760.5963299510936,
			"y": 52.35579958284859,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 65.07194519042969,
			"height": 20,
			"seed": 419550552,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "print (4)",
			"rawText": "print (4)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print (4)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 435,
			"versionNonce": 933950685,
			"isDeleted": false,
			"id": "cn1XWncT",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 763.3247726208776,
			"y": 97.83183473690735,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 64.71994018554688,
			"height": 20,
			"seed": 1032201256,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158212,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "print (5)",
			"rawText": "print (5)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "print (5)",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 271,
			"versionNonce": 609293171,
			"isDeleted": false,
			"id": "MZC97YMDReEb_hszgdVFp",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 790.539286079897,
			"y": -108.49424932404565,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 13.935381596043044,
			"height": 26.40398252549039,
			"seed": 1295574824,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.4668925811909048
				],
				[
					0,
					2.2003528611108436
				],
				[
					0,
					2.9337851623818665
				],
				[
					0,
					4.400677743572828
				],
				[
					0,
					5.134110044843851
				],
				[
					0,
					6.601002626034813
				],
				[
					0,
					7.334434927305836
				],
				[
					0,
					8.067895207225774
				],
				[
					0,
					9.53478778841668
				],
				[
					0,
					10.268220089687759
				],
				[
					0,
					11.735112670878664
				],
				[
					0,
					12.468544972149743
				],
				[
					0,
					13.935437553340648
				],
				[
					0,
					14.668869854611728
				],
				[
					0,
					15.40233013453161
				],
				[
					0,
					16.86922271572257
				],
				[
					0,
					17.602655016993594
				],
				[
					0,
					19.069547598184556
				],
				[
					0,
					19.80297989945558
				],
				[
					0,
					21.26987248064654
				],
				[
					0,
					22.003304781917564
				],
				[
					0,
					22.736765061837446
				],
				[
					-1.4668646025420458,
					22.736765061837446
				],
				[
					-2.2003528611107868,
					22.736765061837446
				],
				[
					-4.4007057222215735,
					22.003304781917564
				],
				[
					-4.4007057222215735,
					20.53644017937546
				],
				[
					-5.867570324763619,
					19.80297989945558
				],
				[
					-6.600946668736924,
					19.80297989945558
				],
				[
					-6.600946668736924,
					18.336087318264617
				],
				[
					-7.334434927305665,
					18.336087318264617
				],
				[
					-7.334434927305665,
					17.602655016993594
				],
				[
					-8.801299529847938,
					17.602655016993594
				],
				[
					-8.067923185874633,
					17.602655016993594
				],
				[
					-7.334434927305665,
					17.602655016993594
				],
				[
					-7.334434927305665,
					19.069547598184556
				],
				[
					-6.600946668736924,
					19.80297989945558
				],
				[
					-5.134082066194878,
					21.26987248064654
				],
				[
					-4.4007057222215735,
					22.003304781917564
				],
				[
					-4.4007057222215735,
					22.736765061837446
				],
				[
					-2.9337292050840915,
					24.203657643028407
				],
				[
					-2.2003528611107868,
					24.93708994429943
				],
				[
					-0.733488258568741,
					26.40398252549039
				],
				[
					0,
					26.40398252549039
				],
				[
					0.733488258568741,
					26.40398252549039
				],
				[
					0.733488258568741,
					25.67052224557051
				],
				[
					2.200352861111014,
					25.67052224557051
				],
				[
					2.200352861111014,
					24.93708994429943
				],
				[
					2.933729205084319,
					24.93708994429943
				],
				[
					2.933729205084319,
					23.470197363108525
				],
				[
					4.400705722221801,
					22.736765061837446
				],
				[
					5.134082066195106,
					22.003304781917564
				],
				[
					5.134082066195106,
					22.003304781917564
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 261,
			"versionNonce": 1402097981,
			"isDeleted": false,
			"id": "H9L1_eSYaxLMZfXFqORhw",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 792.739638941008,
			"y": -58.62006943544674,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 13.935381596043044,
			"height": 16.869194737073713,
			"seed": 469334312,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.4668646025421026
				],
				[
					0.7333763439733048,
					2.2003248824619845
				],
				[
					0.7333763439733048,
					3.667217463652946
				],
				[
					0.7333763439733048,
					4.400649764923969
				],
				[
					0.7333763439733048,
					5.134082066195049
				],
				[
					0.7333763439733048,
					6.600974647385954
				],
				[
					0.7333763439733048,
					7.334406948657033
				],
				[
					0.7333763439733048,
					8.801327508496797
				],
				[
					0.7333763439733048,
					9.534759809767877
				],
				[
					0.7333763439733048,
					11.001624412309923
				],
				[
					2.2003528611107868,
					11.73511267087872
				],
				[
					2.2003528611107868,
					12.468544972149743
				],
				[
					2.2003528611107868,
					13.935409574691846
				],
				[
					2.2003528611107868,
					14.668841875962869
				],
				[
					2.2003528611107868,
					16.13576243580269
				],
				[
					1.4668646025420458,
					16.13576243580269
				],
				[
					1.4668646025420458,
					16.869194737073713
				],
				[
					0.7333763439733048,
					16.869194737073713
				],
				[
					-0.733488258568741,
					15.402330134531667
				],
				[
					-1.4668646025422731,
					15.402330134531667
				],
				[
					-1.4668646025422731,
					14.668841875962869
				],
				[
					-2.200352861111014,
					14.668841875962869
				],
				[
					-2.200352861111014,
					13.201977273420766
				],
				[
					-3.66721746365306,
					13.201977273420766
				],
				[
					-3.66721746365306,
					12.468544972149743
				],
				[
					-2.933841119679755,
					12.468544972149743
				],
				[
					-2.200352861111014,
					13.935409574691846
				],
				[
					-1.4668646025422731,
					14.668841875962869
				],
				[
					0,
					16.13576243580269
				],
				[
					0,
					16.869194737073713
				],
				[
					0.7333763439733048,
					16.869194737073713
				],
				[
					2.2003528611107868,
					16.869194737073713
				],
				[
					2.9337292050840915,
					16.869194737073713
				],
				[
					4.400593807626137,
					16.869194737073713
				],
				[
					5.134082066194878,
					16.869194737073713
				],
				[
					5.867570324763619,
					16.869194737073713
				],
				[
					7.334434927305892,
					16.869194737073713
				],
				[
					8.067811271279197,
					16.869194737073713
				],
				[
					9.53478778841668,
					15.402330134531667
				],
				[
					10.268164132389984,
					15.402330134531667
				],
				[
					10.268164132389984,
					14.668841875962869
				],
				[
					10.268164132389984,
					14.668841875962869
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 277,
			"versionNonce": 576990483,
			"isDeleted": false,
			"id": "Z_NR8gMIOq8To2YgfYak2",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 800.8074502122872,
			"y": -16.813784754073538,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 16.86922271572257,
			"height": 28.604307407952376,
			"seed": 434330920,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.4668646025421026
				],
				[
					0,
					2.2002969038131255
				],
				[
					0,
					3.667217463652946
				],
				[
					0,
					4.400649764923969
				],
				[
					0,
					5.134082066194992
				],
				[
					0,
					6.601002626034813
				],
				[
					0,
					7.334434927305836
				],
				[
					0,
					8.801299529847938
				],
				[
					0,
					9.534731831118961
				],
				[
					0,
					10.268220089687759
				],
				[
					0,
					11.735084692229805
				],
				[
					0,
					12.468516993500884
				],
				[
					0,
					13.935437553340705
				],
				[
					0,
					14.668869854611728
				],
				[
					0,
					16.135734457153774
				],
				[
					0,
					16.869166758424853
				],
				[
					0,
					17.602655016993594
				],
				[
					0,
					19.069519619535697
				],
				[
					0,
					19.80295192080672
				],
				[
					-1.4668646025422731,
					19.80295192080672
				],
				[
					-1.4668646025422731,
					21.26987248064654
				],
				[
					-2.200240946515578,
					21.26987248064654
				],
				[
					-2.200240946515578,
					20.5363842220778
				],
				[
					-2.933729205084319,
					20.5363842220778
				],
				[
					-2.933729205084319,
					19.80295192080672
				],
				[
					-4.400593807626365,
					19.80295192080672
				],
				[
					-4.400593807626365,
					18.336087318264674
				],
				[
					-5.134082066195106,
					18.336087318264674
				],
				[
					-6.600946668737151,
					18.336087318264674
				],
				[
					-7.334434927305892,
					18.336087318264674
				],
				[
					-7.334434927305892,
					19.069519619535697
				],
				[
					-5.86745841016841,
					19.80295192080672
				],
				[
					-5.86745841016841,
					21.26987248064654
				],
				[
					-5.134082066195106,
					22.003304781917564
				],
				[
					-5.134082066195106,
					23.470169384459666
				],
				[
					-3.66721746365306,
					23.470169384459666
				],
				[
					-2.933729205084319,
					24.937089944299487
				],
				[
					-2.200240946515578,
					24.937089944299487
				],
				[
					-2.200240946515578,
					26.403954546841533
				],
				[
					-0.7333763439733048,
					26.403954546841533
				],
				[
					-0.7333763439733048,
					27.137386848112612
				],
				[
					0,
					28.604307407952376
				],
				[
					1.466976517137482,
					28.604307407952376
				],
				[
					1.466976517137482,
					27.870819149383635
				],
				[
					1.466976517137482,
					27.137386848112612
				],
				[
					1.466976517137482,
					25.67052224557051
				],
				[
					2.2003528611107868,
					24.937089944299487
				],
				[
					2.2003528611107868,
					24.20360168573069
				],
				[
					2.9338411196795278,
					22.736737083188643
				],
				[
					4.4007057222215735,
					22.003304781917564
				],
				[
					5.1341939807903145,
					20.5363842220778
				],
				[
					6.60105858333236,
					19.80295192080672
				],
				[
					7.334434927305665,
					18.336087318264674
				],
				[
					8.801411444443374,
					17.602655016993594
				],
				[
					8.801411444443374,
					16.869166758424853
				],
				[
					9.53478778841668,
					16.869166758424853
				],
				[
					9.53478778841668,
					15.40230215588275
				],
				[
					9.53478778841668,
					15.40230215588275
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 264,
			"versionNonce": 1192173981,
			"isDeleted": false,
			"id": "1yr-sGNoiMbgPeSok4lZE",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 803.007803073398,
			"y": 30.860042273414535,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 11.735028734932257,
			"height": 18.336087318264674,
			"seed": 1892413736,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.733488258568741,
					0
				],
				[
					2.2003528611107868,
					0.7334323012710797
				],
				[
					2.2003528611107868,
					1.4668646025421026
				],
				[
					2.2003528611107868,
					2.9337851623819233
				],
				[
					2.2003528611107868,
					3.667217463652946
				],
				[
					2.2003528611107868,
					4.400649764923969
				],
				[
					2.2003528611107868,
					5.867514367466072
				],
				[
					2.2003528611107868,
					8.067867228576915
				],
				[
					2.2003528611107868,
					8.801299529847938
				],
				[
					2.2003528611107868,
					9.534731831119018
				],
				[
					2.2003528611107868,
					11.001652390958839
				],
				[
					2.2003528611107868,
					11.735084692229862
				],
				[
					2.2003528611107868,
					13.201949294771964
				],
				[
					2.2003528611107868,
					13.935437553340705
				],
				[
					2.2003528611107868,
					15.402302155882808
				],
				[
					2.2003528611107868,
					16.13573445715383
				],
				[
					2.2003528611107868,
					16.869166758424853
				],
				[
					1.4668646025420458,
					16.869166758424853
				],
				[
					0.733488258568741,
					16.869166758424853
				],
				[
					0,
					16.869166758424853
				],
				[
					-1.4668646025420458,
					16.13573445715383
				],
				[
					-2.2003528611107868,
					14.668869854611728
				],
				[
					-3.66721746365306,
					14.668869854611728
				],
				[
					-4.400593807626365,
					13.935437553340705
				],
				[
					-2.9337292050840915,
					13.935437553340705
				],
				[
					-2.9337292050840915,
					15.402302155882808
				],
				[
					-2.2003528611107868,
					15.402302155882808
				],
				[
					-2.2003528611107868,
					16.13573445715383
				],
				[
					-0.7333763439733048,
					16.13573445715383
				],
				[
					-0.7333763439733048,
					16.869166758424853
				],
				[
					0,
					16.869166758424853
				],
				[
					0,
					18.336087318264674
				],
				[
					0.733488258568741,
					18.336087318264674
				],
				[
					2.2003528611107868,
					18.336087318264674
				],
				[
					2.9338411196795278,
					17.60265501699365
				],
				[
					4.4007057222215735,
					17.60265501699365
				],
				[
					4.4007057222215735,
					16.869166758424853
				],
				[
					5.134082066194878,
					16.13573445715383
				],
				[
					5.134082066194878,
					14.668869854611728
				],
				[
					6.601058583332588,
					14.668869854611728
				],
				[
					6.601058583332588,
					13.935437553340705
				],
				[
					7.334434927305892,
					13.935437553340705
				],
				[
					7.334434927305892,
					12.468516993500884
				],
				[
					7.334434927305892,
					11.735084692229862
				],
				[
					7.334434927305892,
					11.735084692229862
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 276,
			"versionNonce": 1310921395,
			"isDeleted": false,
			"id": "oWhianSA-BIhTntrquS2M",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 804.47466767594,
			"y": 69.73251381375695,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 11.735140649527466,
			"height": 24.203657643028464,
			"seed": 588056104,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.733488258568741,
					0
				],
				[
					0.733488258568741,
					1.4669205598398776
				],
				[
					1.466976517137482,
					2.2003528611109004
				],
				[
					1.466976517137482,
					3.667217463652946
				],
				[
					1.466976517137482,
					4.400705722221687
				],
				[
					1.466976517137482,
					5.134138023492824
				],
				[
					2.9338411196795278,
					6.6010026260348695
				],
				[
					2.9338411196795278,
					7.334434927305892
				],
				[
					2.9338411196795278,
					8.801355487145656
				],
				[
					2.9338411196795278,
					9.534787788416793
				],
				[
					2.9338411196795278,
					11.001652390958839
				],
				[
					2.9338411196795278,
					11.73514064952758
				],
				[
					2.9338411196795278,
					12.468572950798603
				],
				[
					2.9338411196795278,
					13.935437553340762
				],
				[
					2.9338411196795278,
					14.668869854611785
				],
				[
					2.9338411196795278,
					16.13579041445155
				],
				[
					2.9338411196795278,
					16.86922271572257
				],
				[
					2.9338411196795278,
					17.602655016993594
				],
				[
					2.9338411196795278,
					19.069575576833472
				],
				[
					2.9338411196795278,
					19.803007878104495
				],
				[
					3.6672174636528325,
					19.803007878104495
				],
				[
					3.6672174636528325,
					21.26987248064654
				],
				[
					3.6672174636528325,
					22.003304781917677
				],
				[
					3.6672174636528325,
					23.47022534175744
				],
				[
					2.2003528611107868,
					22.73679304048642
				],
				[
					1.466976517137482,
					22.73679304048642
				],
				[
					1.466976517137482,
					22.003304781917677
				],
				[
					0,
					22.003304781917677
				],
				[
					0,
					20.536440179375518
				],
				[
					-0.7333763439733048,
					20.536440179375518
				],
				[
					-1.4668646025420458,
					20.536440179375518
				],
				[
					-1.4668646025420458,
					19.803007878104495
				],
				[
					-2.9337292050840915,
					19.803007878104495
				],
				[
					-2.9337292050840915,
					18.33608731826473
				],
				[
					-3.6672174636528325,
					18.33608731826473
				],
				[
					-3.6672174636528325,
					19.069575576833472
				],
				[
					-2.2002409465153505,
					19.069575576833472
				],
				[
					-2.2002409465153505,
					19.803007878104495
				],
				[
					-1.4668646025420458,
					19.803007878104495
				],
				[
					-1.4668646025420458,
					21.26987248064654
				],
				[
					-0.7333763439733048,
					21.26987248064654
				],
				[
					-0.7333763439733048,
					22.003304781917677
				],
				[
					0.733488258568741,
					22.003304781917677
				],
				[
					0.733488258568741,
					23.47022534175744
				],
				[
					1.466976517137482,
					23.47022534175744
				],
				[
					2.9338411196795278,
					23.47022534175744
				],
				[
					2.9338411196795278,
					24.203657643028464
				],
				[
					3.6672174636528325,
					24.203657643028464
				],
				[
					5.134193980790542,
					22.73679304048642
				],
				[
					5.134193980790542,
					22.003304781917677
				],
				[
					5.867570324763847,
					22.003304781917677
				],
				[
					5.867570324763847,
					20.536440179375518
				],
				[
					6.601058583332588,
					20.536440179375518
				],
				[
					6.601058583332588,
					19.803007878104495
				],
				[
					8.067923185874633,
					19.803007878104495
				],
				[
					8.067923185874633,
					18.33608731826473
				],
				[
					8.067923185874633,
					18.33608731826473
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 283,
			"versionNonce": 1733486077,
			"isDeleted": false,
			"id": "Dds4D38o1_shS8nqegBAR",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 841.880330571038,
			"y": 68.2656492112149,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 22.736681125890982,
			"height": 35.93874233525821,
			"seed": 435323688,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7333763439733048,
					0
				],
				[
					2.200352861111014,
					0
				],
				[
					2.933729205084319,
					0
				],
				[
					4.400593807626365,
					0
				],
				[
					5.134082066195106,
					0
				],
				[
					6.600946668737151,
					0
				],
				[
					7.334434927305892,
					0
				],
				[
					8.067811271279197,
					0
				],
				[
					9.53478778841668,
					1.4669205598397639
				],
				[
					10.268164132389984,
					1.4669205598397639
				],
				[
					11.735028734932257,
					1.4669205598397639
				],
				[
					12.468516993500998,
					1.4669205598397639
				],
				[
					13.935381596043044,
					1.4669205598397639
				],
				[
					14.668869854611785,
					2.2003528611107868
				],
				[
					15.40224619858509,
					2.2003528611107868
				],
				[
					16.86922271572257,
					2.2003528611107868
				],
				[
					16.86922271572257,
					3.6672174636528325
				],
				[
					17.602599059695876,
					4.400705722221687
				],
				[
					19.069463662237922,
					4.400705722221687
				],
				[
					19.80295192080689,
					5.867570324763733
				],
				[
					20.53644017937563,
					6.601002626034756
				],
				[
					20.53644017937563,
					7.334434927305779
				],
				[
					22.003304781917677,
					8.801355487145656
				],
				[
					22.003304781917677,
					9.53478778841668
				],
				[
					22.003304781917677,
					11.001652390958725
				],
				[
					22.003304781917677,
					11.735140649527466
				],
				[
					22.003304781917677,
					13.202005252069625
				],
				[
					22.736681125890982,
					13.935437553340648
				],
				[
					22.736681125890982,
					14.668869854611671
				],
				[
					22.736681125890982,
					16.135790414451435
				],
				[
					22.736681125890982,
					16.86922271572257
				],
				[
					22.736681125890982,
					18.336087318264617
				],
				[
					22.736681125890982,
					19.06957557683336
				],
				[
					22.736681125890982,
					20.536440179375404
				],
				[
					22.736681125890982,
					21.26987248064654
				],
				[
					22.736681125890982,
					22.003304781917564
				],
				[
					22.736681125890982,
					23.470225341757327
				],
				[
					21.269816523348936,
					23.470225341757327
				],
				[
					21.269816523348936,
					24.20365764302835
				],
				[
					20.53644017937563,
					24.20365764302835
				],
				[
					20.53644017937563,
					25.67052224557051
				],
				[
					19.80295192080689,
					26.40401050413925
				],
				[
					19.80295192080689,
					27.137442805410274
				],
				[
					18.336087318264617,
					27.137442805410274
				],
				[
					17.602599059695876,
					27.137442805410274
				],
				[
					17.602599059695876,
					28.60430740795232
				],
				[
					16.13573445715383,
					28.60430740795232
				],
				[
					15.40224619858509,
					28.60430740795232
				],
				[
					15.40224619858509,
					29.337739709223456
				],
				[
					14.668869854611785,
					29.337739709223456
				],
				[
					13.202005252069739,
					30.80466026906322
				],
				[
					12.468516993500998,
					30.80466026906322
				],
				[
					11.001652390958952,
					30.80466026906322
				],
				[
					11.001652390958952,
					31.538092570334243
				],
				[
					10.268164132389984,
					31.538092570334243
				],
				[
					8.801299529847938,
					31.538092570334243
				],
				[
					8.067811271279197,
					33.00495717287629
				],
				[
					7.334434927305892,
					33.00495717287629
				],
				[
					5.867570324763847,
					33.00495717287629
				],
				[
					5.134082066195106,
					33.73844543144514
				],
				[
					3.66721746365306,
					33.73844543144514
				],
				[
					3.66721746365306,
					34.471877732716166
				],
				[
					2.933729205084319,
					34.471877732716166
				],
				[
					1.4668646025420458,
					34.471877732716166
				],
				[
					0.7333763439733048,
					34.471877732716166
				],
				[
					0.7333763439733048,
					35.93874233525821
				],
				[
					0.7333763439733048,
					35.93874233525821
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 243,
			"versionNonce": 406078547,
			"isDeleted": false,
			"id": "9Lv3brJQAtesCHbbYCPnO",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 844.080683432149,
			"y": 60.931214283909014,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 8.801299529847938,
			"height": 13.202005252069682,
			"seed": 1363036712,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.7334323012710797
				],
				[
					-0.7334882585689684,
					-0.7334323012710797
				],
				[
					-1.4669765171377094,
					-0.7334323012710797
				],
				[
					-1.4669765171377094,
					0
				],
				[
					-2.200352861111014,
					0
				],
				[
					-2.200352861111014,
					1.4669205598397639
				],
				[
					-3.66721746365306,
					1.4669205598397639
				],
				[
					-3.66721746365306,
					2.2003528611108436
				],
				[
					-4.400705722221801,
					3.6672174636528894
				],
				[
					-5.867570324763847,
					3.6672174636528894
				],
				[
					-5.867570324763847,
					4.400705722221687
				],
				[
					-5.867570324763847,
					5.13413802349271
				],
				[
					-5.867570324763847,
					6.601002626034813
				],
				[
					-5.134193980790542,
					7.334434927305892
				],
				[
					-4.400705722221801,
					7.334434927305892
				],
				[
					-4.400705722221801,
					8.801355487145656
				],
				[
					-2.933841119679755,
					8.801355487145656
				],
				[
					-2.200352861111014,
					8.801355487145656
				],
				[
					-2.200352861111014,
					9.53478778841668
				],
				[
					-1.4669765171377094,
					9.53478778841668
				],
				[
					0,
					11.001652390958725
				],
				[
					0.7333763439733048,
					11.001652390958725
				],
				[
					0.7333763439733048,
					11.73514064952758
				],
				[
					2.2002409465153505,
					11.73514064952758
				],
				[
					2.2002409465153505,
					12.468572950798603
				],
				[
					2.9337292050840915,
					12.468572950798603
				],
				[
					2.9337292050840915,
					12.468572950798603
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 342,
			"versionNonce": 1734286941,
			"isDeleted": false,
			"id": "9ShYgZGbOoK8Kc_VKfN9h",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 840.5967494340833,
			"y": 24.185687277557875,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 20.463018795538908,
			"height": 32.3448772414272,
			"seed": 1049056296,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.6600388960832233,
					0
				],
				[
					1.9803181345785823,
					0
				],
				[
					2.640357030661806,
					0
				],
				[
					3.9605355459926064,
					0
				],
				[
					4.620675165240184,
					0
				],
				[
					5.940853680570984,
					0
				],
				[
					6.600993299818561,
					0
				],
				[
					7.261032195901785,
					0
				],
				[
					8.58131143439694,
					1.3202288769129773
				],
				[
					9.241350330480163,
					1.3202288769129773
				],
				[
					10.561528845811168,
					1.3202288769129773
				],
				[
					11.221668465058745,
					1.3202288769129773
				],
				[
					12.541846980389545,
					1.3202288769129773
				],
				[
					13.201986599637122,
					1.9803181345783776
				],
				[
					13.862025495720346,
					1.9803181345783776
				],
				[
					15.1823047342155,
					1.9803181345783776
				],
				[
					15.1823047342155,
					3.300496649909178
				],
				[
					15.842343630298723,
					3.9606362691568573
				],
				[
					17.162522145629524,
					3.9606362691568573
				],
				[
					17.822661764877306,
					5.280814784487657
				],
				[
					18.482801384124883,
					5.940904042153058
				],
				[
					18.482801384124883,
					6.600993299818458
				],
				[
					19.802979899455682,
					7.921222176731538
				],
				[
					19.802979899455682,
					8.581311434396937
				],
				[
					19.802979899455682,
					9.901489949727738
				],
				[
					19.802979899455682,
					10.561629568975315
				],
				[
					19.802979899455682,
					11.881808084306218
				],
				[
					20.463018795538908,
					12.541897341971618
				],
				[
					20.463018795538908,
					13.201986599637019
				],
				[
					20.463018795538908,
					14.522215476549995
				],
				[
					20.463018795538908,
					15.182304734215498
				],
				[
					20.463018795538908,
					16.502483249546298
				],
				[
					20.463018795538908,
					17.162622868793875
				],
				[
					20.463018795538908,
					18.482801384124677
				],
				[
					20.463018795538908,
					19.142890641790178
				],
				[
					20.463018795538908,
					19.80297989945558
				],
				[
					20.463018795538908,
					21.123208776368557
				],
				[
					19.142840280208105,
					21.123208776368557
				],
				[
					19.142840280208105,
					21.783298034033955
				],
				[
					18.482801384124883,
					21.783298034033955
				],
				[
					18.482801384124883,
					23.10347654936486
				],
				[
					17.822661764877306,
					23.763616168612437
				],
				[
					17.822661764877306,
					24.423705426277838
				],
				[
					16.5024832495463,
					24.423705426277838
				],
				[
					15.842343630298723,
					24.423705426277838
				],
				[
					15.842343630298723,
					25.743883941608637
				],
				[
					14.522165114967923,
					25.743883941608637
				],
				[
					13.862025495720346,
					25.743883941608637
				],
				[
					13.862025495720346,
					26.40397319927414
				],
				[
					13.201986599637122,
					26.40397319927414
				],
				[
					11.881808084306321,
					27.724202076187115
				],
				[
					11.221668465058745,
					27.724202076187115
				],
				[
					9.901489949727944,
					27.724202076187115
				],
				[
					9.901489949727944,
					28.384291333852516
				],
				[
					9.241350330480163,
					28.384291333852516
				],
				[
					7.9211718151493615,
					28.384291333852516
				],
				[
					7.261032195901785,
					29.70446984918332
				],
				[
					6.600993299818561,
					29.70446984918332
				],
				[
					5.28081478448776,
					29.70446984918332
				],
				[
					4.620675165240184,
					30.364609468430995
				],
				[
					3.300496649909383,
					30.364609468430995
				],
				[
					3.300496649909383,
					31.024698726096396
				],
				[
					2.640357030661806,
					31.024698726096396
				],
				[
					1.3201785153308006,
					31.024698726096396
				],
				[
					0.6600388960832233,
					31.024698726096396
				],
				[
					0.6600388960832233,
					32.3448772414272
				],
				[
					0.6600388960832233,
					32.3448772414272
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 302,
			"versionNonce": 409879027,
			"isDeleted": false,
			"id": "rqyin-2oPv7W5S2-P-Prd",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 842.5770675686617,
			"y": 17.584693977739313,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 7.9211718151493615,
			"height": 11.88180808430627,
			"seed": 1306169128,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.6600892576654513
				],
				[
					-0.6601396192477819,
					-0.6600892576654513
				],
				[
					-1.3202792384953592,
					-0.6600892576654513
				],
				[
					-1.3202792384953592,
					0
				],
				[
					-1.9803181345785823,
					0
				],
				[
					-1.9803181345785823,
					1.3202288769129773
				],
				[
					-3.300496649909383,
					1.3202288769129773
				],
				[
					-3.300496649909383,
					1.9803181345784286
				],
				[
					-3.9606362691569603,
					3.300496649909229
				],
				[
					-5.28081478448776,
					3.300496649909229
				],
				[
					-5.28081478448776,
					3.9606362691568573
				],
				[
					-5.28081478448776,
					4.620725526822257
				],
				[
					-5.28081478448776,
					5.940904042153109
				],
				[
					-4.620775888404538,
					6.60099329981856
				],
				[
					-3.9606362691569603,
					6.60099329981856
				],
				[
					-3.9606362691569603,
					7.921222176731538
				],
				[
					-2.6404577538261598,
					7.921222176731538
				],
				[
					-1.9803181345785823,
					7.921222176731538
				],
				[
					-1.9803181345785823,
					8.581311434396937
				],
				[
					-1.3202792384953592,
					8.581311434396937
				],
				[
					0,
					9.901489949727738
				],
				[
					0.6600388960832233,
					9.901489949727738
				],
				[
					0.6600388960832233,
					10.561629568975418
				],
				[
					1.9802174114140239,
					10.561629568975418
				],
				[
					1.9802174114140239,
					11.221718826640817
				],
				[
					2.640357030661601,
					11.221718826640817
				],
				[
					2.640357030661601,
					11.221718826640817
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 366,
			"versionNonce": 503663293,
			"isDeleted": false,
			"id": "hfFJzaICJZtTMq9qhVpCQ",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 840.8209620360809,
			"y": -22.017165664017774,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 21.852438954026546,
			"height": 34.54106466187,
			"seed": 1101510440,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7048549301575255,
					0
				],
				[
					2.114779914821973,
					0
				],
				[
					2.8196348449794986,
					0
				],
				[
					4.229452267469139,
					0
				],
				[
					4.934414759801252,
					0
				],
				[
					6.344232182290893,
					0
				],
				[
					7.049194674623008,
					0
				],
				[
					7.7540496047805325,
					0
				],
				[
					9.163974589444763,
					1.4098712035769343
				],
				[
					9.868829519602286,
					1.4098712035769343
				],
				[
					11.278646942092145,
					1.4098712035769343
				],
				[
					11.98360943442426,
					1.4098712035769343
				],
				[
					13.393426856913901,
					1.4098712035769343
				],
				[
					14.098389349246016,
					2.1147799148217543
				],
				[
					14.80324427940354,
					2.1147799148217543
				],
				[
					16.21316926406777,
					2.1147799148217543
				],
				[
					16.21316926406777,
					3.5245973373113944
				],
				[
					16.918024194225296,
					4.229559829643618
				],
				[
					18.327841616714935,
					4.229559829643618
				],
				[
					19.032804109047266,
					5.639377252133258
				],
				[
					19.73776660137938,
					6.344285963378078
				],
				[
					19.73776660137938,
					7.049194674622899
				],
				[
					21.147584023869022,
					8.459065878199942
				],
				[
					21.147584023869022,
					9.163974589444763
				],
				[
					21.147584023869022,
					10.573792011934401
				],
				[
					21.147584023869022,
					11.278754504266516
				],
				[
					21.147584023869022,
					12.688571926756266
				],
				[
					21.852438954026546,
					13.393480638001085
				],
				[
					21.852438954026546,
					14.098389349245906
				],
				[
					21.852438954026546,
					15.50826055282284
				],
				[
					21.852438954026546,
					16.21316926406777
				],
				[
					21.852438954026546,
					17.62298668655741
				],
				[
					21.852438954026546,
					18.327949178889526
				],
				[
					21.852438954026546,
					19.737766601379164
				],
				[
					21.852438954026546,
					20.442675312624093
				],
				[
					21.852438954026546,
					21.147584023868912
				],
				[
					21.852438954026546,
					22.55745522744585
				],
				[
					20.442621531536908,
					22.55745522744585
				],
				[
					20.442621531536908,
					23.26236393869067
				],
				[
					19.73776660137938,
					23.26236393869067
				],
				[
					19.73776660137938,
					24.672181361180417
				],
				[
					19.032804109047266,
					25.377143853512532
				],
				[
					19.032804109047266,
					26.08205256475735
				],
				[
					17.62298668655741,
					26.08205256475735
				],
				[
					16.918024194225296,
					26.08205256475735
				],
				[
					16.918024194225296,
					27.491869987246993
				],
				[
					15.508206771735654,
					27.491869987246993
				],
				[
					14.80324427940354,
					27.491869987246993
				],
				[
					14.80324427940354,
					28.19677869849192
				],
				[
					14.098389349246016,
					28.19677869849192
				],
				[
					12.688571926756374,
					29.606649902068856
				],
				[
					11.98360943442426,
					29.606649902068856
				],
				[
					10.57379201193462,
					29.606649902068856
				],
				[
					10.57379201193462,
					30.311558613313675
				],
				[
					9.868829519602286,
					30.311558613313675
				],
				[
					8.459012097112648,
					30.311558613313675
				],
				[
					7.7540496047805325,
					31.721376035803317
				],
				[
					7.049194674623008,
					31.721376035803317
				],
				[
					5.639377252133367,
					31.721376035803317
				],
				[
					4.934414759801252,
					32.42633852813554
				],
				[
					3.524597337311613,
					32.42633852813554
				],
				[
					3.524597337311613,
					33.13124723938036
				],
				[
					2.8196348449794986,
					33.13124723938036
				],
				[
					1.4098174224896398,
					33.13124723938036
				],
				[
					0.7048549301575255,
					33.13124723938036
				],
				[
					0.7048549301575255,
					34.54106466187
				],
				[
					0.7048549301575255,
					34.54106466187
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 326,
			"versionNonce": 668437395,
			"isDeleted": false,
			"id": "O0BL4hFMxx25ppy_EHWPp",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 842.9357419509032,
			"y": -29.066360338640777,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 8.459012097112648,
			"height": 12.688571926756321,
			"seed": 1962316328,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.7049087112448746
				],
				[
					-0.704962492332333,
					-0.7049087112448746
				],
				[
					-1.4099249846644475,
					-0.7049087112448746
				],
				[
					-1.4099249846644475,
					0
				],
				[
					-2.114779914821973,
					0
				],
				[
					-2.114779914821973,
					1.4098712035769343
				],
				[
					-3.524597337311613,
					1.4098712035769343
				],
				[
					-3.524597337311613,
					2.114779914821809
				],
				[
					-4.229559829643728,
					3.5245973373114494
				],
				[
					-5.639377252133367,
					3.5245973373114494
				],
				[
					-5.639377252133367,
					4.229559829643618
				],
				[
					-5.639377252133367,
					4.934468540888438
				],
				[
					-5.639377252133367,
					6.344285963378133
				],
				[
					-4.934522321975842,
					7.049194674623008
				],
				[
					-4.229559829643728,
					7.049194674623008
				],
				[
					-4.229559829643728,
					8.459065878199942
				],
				[
					-2.819742407154087,
					8.459065878199942
				],
				[
					-2.114779914821973,
					8.459065878199942
				],
				[
					-2.114779914821973,
					9.163974589444763
				],
				[
					-1.4099249846644475,
					9.163974589444763
				],
				[
					0,
					10.573792011934401
				],
				[
					0.7048549301575255,
					10.573792011934401
				],
				[
					0.7048549301575255,
					11.278754504266626
				],
				[
					2.114672352647166,
					11.278754504266626
				],
				[
					2.114672352647166,
					11.983663215511445
				],
				[
					2.8196348449792796,
					11.983663215511445
				],
				[
					2.8196348449792796,
					11.983663215511445
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 333,
			"versionNonce": 199682845,
			"isDeleted": false,
			"id": "XCeYZZZ2QP47Q6lObOZXM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 836.3794484182608,
			"y": -68.88828952513441,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 22.736681125890982,
			"height": 35.93874233525821,
			"seed": 1525795416,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7333763439733048,
					0
				],
				[
					2.200352861111014,
					0
				],
				[
					2.933729205084319,
					0
				],
				[
					4.400593807626365,
					0
				],
				[
					5.134082066195106,
					0
				],
				[
					6.600946668737151,
					0
				],
				[
					7.334434927305892,
					0
				],
				[
					8.067811271279197,
					0
				],
				[
					9.53478778841668,
					1.4669205598397639
				],
				[
					10.268164132389984,
					1.4669205598397639
				],
				[
					11.735028734932257,
					1.4669205598397639
				],
				[
					12.468516993500998,
					1.4669205598397639
				],
				[
					13.935381596043044,
					1.4669205598397639
				],
				[
					14.668869854611785,
					2.2003528611107868
				],
				[
					15.40224619858509,
					2.2003528611107868
				],
				[
					16.86922271572257,
					2.2003528611107868
				],
				[
					16.86922271572257,
					3.6672174636528325
				],
				[
					17.602599059695876,
					4.400705722221687
				],
				[
					19.069463662237922,
					4.400705722221687
				],
				[
					19.80295192080689,
					5.867570324763733
				],
				[
					20.53644017937563,
					6.601002626034756
				],
				[
					20.53644017937563,
					7.334434927305779
				],
				[
					22.003304781917677,
					8.801355487145656
				],
				[
					22.003304781917677,
					9.53478778841668
				],
				[
					22.003304781917677,
					11.001652390958725
				],
				[
					22.003304781917677,
					11.735140649527466
				],
				[
					22.003304781917677,
					13.202005252069625
				],
				[
					22.736681125890982,
					13.935437553340648
				],
				[
					22.736681125890982,
					14.668869854611671
				],
				[
					22.736681125890982,
					16.135790414451435
				],
				[
					22.736681125890982,
					16.86922271572257
				],
				[
					22.736681125890982,
					18.336087318264617
				],
				[
					22.736681125890982,
					19.06957557683336
				],
				[
					22.736681125890982,
					20.536440179375404
				],
				[
					22.736681125890982,
					21.26987248064654
				],
				[
					22.736681125890982,
					22.003304781917564
				],
				[
					22.736681125890982,
					23.470225341757327
				],
				[
					21.269816523348936,
					23.470225341757327
				],
				[
					21.269816523348936,
					24.20365764302835
				],
				[
					20.53644017937563,
					24.20365764302835
				],
				[
					20.53644017937563,
					25.67052224557051
				],
				[
					19.80295192080689,
					26.40401050413925
				],
				[
					19.80295192080689,
					27.137442805410274
				],
				[
					18.336087318264617,
					27.137442805410274
				],
				[
					17.602599059695876,
					27.137442805410274
				],
				[
					17.602599059695876,
					28.60430740795232
				],
				[
					16.13573445715383,
					28.60430740795232
				],
				[
					15.40224619858509,
					28.60430740795232
				],
				[
					15.40224619858509,
					29.337739709223456
				],
				[
					14.668869854611785,
					29.337739709223456
				],
				[
					13.202005252069739,
					30.80466026906322
				],
				[
					12.468516993500998,
					30.80466026906322
				],
				[
					11.001652390958952,
					30.80466026906322
				],
				[
					11.001652390958952,
					31.538092570334243
				],
				[
					10.268164132389984,
					31.538092570334243
				],
				[
					8.801299529847938,
					31.538092570334243
				],
				[
					8.067811271279197,
					33.00495717287629
				],
				[
					7.334434927305892,
					33.00495717287629
				],
				[
					5.867570324763847,
					33.00495717287629
				],
				[
					5.134082066195106,
					33.73844543144514
				],
				[
					3.66721746365306,
					33.73844543144514
				],
				[
					3.66721746365306,
					34.471877732716166
				],
				[
					2.933729205084319,
					34.471877732716166
				],
				[
					1.4668646025420458,
					34.471877732716166
				],
				[
					0.7333763439733048,
					34.471877732716166
				],
				[
					0.7333763439733048,
					35.93874233525821
				],
				[
					0.7333763439733048,
					35.93874233525821
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 293,
			"versionNonce": 983998771,
			"isDeleted": false,
			"id": "0JOoI54aB2wjYhYMn2rrq",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 838.5798012793721,
			"y": -76.2227244524403,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 8.801299529847938,
			"height": 13.202005252069682,
			"seed": 737591128,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.7334323012710797
				],
				[
					-0.7334882585689684,
					-0.7334323012710797
				],
				[
					-1.4669765171377094,
					-0.7334323012710797
				],
				[
					-1.4669765171377094,
					0
				],
				[
					-2.200352861111014,
					0
				],
				[
					-2.200352861111014,
					1.4669205598397639
				],
				[
					-3.66721746365306,
					1.4669205598397639
				],
				[
					-3.66721746365306,
					2.2003528611108436
				],
				[
					-4.400705722221801,
					3.6672174636528894
				],
				[
					-5.867570324763847,
					3.6672174636528894
				],
				[
					-5.867570324763847,
					4.400705722221687
				],
				[
					-5.867570324763847,
					5.13413802349271
				],
				[
					-5.867570324763847,
					6.601002626034813
				],
				[
					-5.134193980790542,
					7.334434927305892
				],
				[
					-4.400705722221801,
					7.334434927305892
				],
				[
					-4.400705722221801,
					8.801355487145656
				],
				[
					-2.933841119679755,
					8.801355487145656
				],
				[
					-2.200352861111014,
					8.801355487145656
				],
				[
					-2.200352861111014,
					9.53478778841668
				],
				[
					-1.4669765171377094,
					9.53478778841668
				],
				[
					0,
					11.001652390958725
				],
				[
					0.7333763439733048,
					11.001652390958725
				],
				[
					0.7333763439733048,
					11.73514064952758
				],
				[
					2.2002409465153505,
					11.73514064952758
				],
				[
					2.2002409465153505,
					12.468572950798603
				],
				[
					2.9337292050840915,
					12.468572950798603
				],
				[
					2.9337292050840915,
					12.468572950798603
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 351,
			"versionNonce": 561348477,
			"isDeleted": false,
			"id": "eL1OA4Xp1nvxRtTINgEFd",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 831.4899580319725,
			"y": -109.78998932895627,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 18.568280912788765,
			"height": 29.349959197585324,
			"seed": 1454591528,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.5989237344839919,
					0
				],
				[
					1.79695399720599,
					0
				],
				[
					2.395877731689982,
					0
				],
				[
					3.59381659753488,
					0
				],
				[
					4.192831728895786,
					0
				],
				[
					5.390770594740684,
					0
				],
				[
					5.989785726101591,
					0
				],
				[
					6.588709460585583,
					0
				],
				[
					7.786739723307395,
					1.1979845642833555
				],
				[
					8.385663457791386,
					1.1979845642833555
				],
				[
					9.583602323636471,
					1.1979845642833555
				],
				[
					10.182617454997377,
					1.1979845642833555
				],
				[
					11.380556320842276,
					1.1979845642833555
				],
				[
					11.979571452203182,
					1.7969539972058046
				],
				[
					12.578495186687173,
					1.7969539972058046
				],
				[
					13.776525449408986,
					1.7969539972058046
				],
				[
					13.776525449408986,
					2.994892863050703
				],
				[
					14.375449183892977,
					3.593907994411702
				],
				[
					15.573388049737876,
					3.593907994411702
				],
				[
					16.172403181098968,
					4.791846860256601
				],
				[
					16.771418312459875,
					5.390816293179049
				],
				[
					16.771418312459875,
					5.989785726101498
				],
				[
					17.969357178304772,
					7.187770290384947
				],
				[
					17.969357178304772,
					7.786739723307396
				],
				[
					17.969357178304772,
					8.984678589152294
				],
				[
					17.969357178304772,
					9.583693720513201
				],
				[
					17.969357178304772,
					10.781632586358192
				],
				[
					18.568280912788765,
					11.38060201928064
				],
				[
					18.568280912788765,
					11.979571452203091
				],
				[
					18.568280912788765,
					13.177556016486445
				],
				[
					18.568280912788765,
					13.776525449408988
				],
				[
					18.568280912788765,
					14.974464315253886
				],
				[
					18.568280912788765,
					15.573479446614792
				],
				[
					18.568280912788765,
					16.77141831245969
				],
				[
					18.568280912788765,
					17.37038774538223
				],
				[
					18.568280912788765,
					17.96935717830468
				],
				[
					18.568280912788765,
					19.167341742588036
				],
				[
					17.370342046943865,
					19.167341742588036
				],
				[
					17.370342046943865,
					19.766311175510488
				],
				[
					16.771418312459875,
					19.766311175510488
				],
				[
					16.771418312459875,
					20.964250041355477
				],
				[
					16.172403181098968,
					21.563265172716385
				],
				[
					16.172403181098968,
					22.162234605638833
				],
				[
					14.974464315253885,
					22.162234605638833
				],
				[
					14.375449183892977,
					22.162234605638833
				],
				[
					14.375449183892977,
					23.36017347148373
				],
				[
					13.17751031804808,
					23.36017347148373
				],
				[
					12.578495186687173,
					23.36017347148373
				],
				[
					12.578495186687173,
					23.959142904406274
				],
				[
					11.979571452203182,
					23.959142904406274
				],
				[
					10.781632586358283,
					25.15712746868963
				],
				[
					10.182617454997377,
					25.15712746868963
				],
				[
					8.984678589152479,
					25.15712746868963
				],
				[
					8.984678589152479,
					25.75609690161208
				],
				[
					8.385663457791386,
					25.75609690161208
				],
				[
					7.1877245919464885,
					25.75609690161208
				],
				[
					6.588709460585583,
					26.954035767456975
				],
				[
					5.989785726101591,
					26.954035767456975
				],
				[
					4.791846860256692,
					26.954035767456975
				],
				[
					4.192831728895786,
					27.553050898817975
				],
				[
					2.994892863050888,
					27.553050898817975
				],
				[
					2.994892863050888,
					28.152020331740424
				],
				[
					2.395877731689982,
					28.152020331740424
				],
				[
					1.1979388658448982,
					28.152020331740424
				],
				[
					0.5989237344839919,
					28.152020331740424
				],
				[
					0.5989237344839919,
					29.349959197585324
				],
				[
					0.5989237344839919,
					29.349959197585324
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 311,
			"versionNonce": 2051146451,
			"isDeleted": false,
			"id": "BQ5M-uINfA62tfw3f8vIe",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 833.2869120291783,
			"y": -115.77977505505785,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 7.18772459194649,
			"height": 10.781632586358239,
			"seed": 846678312,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.5989694329224956
				],
				[
					-0.599015131361092,
					-0.5989694329224956
				],
				[
					-1.1980302627219983,
					-0.5989694329224956
				],
				[
					-1.1980302627219983,
					0
				],
				[
					-1.7969539972059902,
					0
				],
				[
					-1.7969539972059902,
					1.1979845642833555
				],
				[
					-2.9948928630508886,
					1.1979845642833555
				],
				[
					-2.9948928630508886,
					1.796953997205851
				],
				[
					-3.593907994411795,
					2.994892863050749
				],
				[
					-4.791846860256693,
					2.994892863050749
				],
				[
					-4.791846860256693,
					3.593907994411702
				],
				[
					-4.791846860256693,
					4.192877427334151
				],
				[
					-4.791846860256693,
					5.390816293179096
				],
				[
					-4.192923125772701,
					5.989785726101592
				],
				[
					-3.593907994411795,
					5.989785726101592
				],
				[
					-3.593907994411795,
					7.187770290384947
				],
				[
					-2.3959691285668967,
					7.187770290384947
				],
				[
					-1.7969539972059902,
					7.187770290384947
				],
				[
					-1.7969539972059902,
					7.786739723307396
				],
				[
					-1.1980302627219983,
					7.786739723307396
				],
				[
					0,
					8.984678589152294
				],
				[
					0.598923734483992,
					8.984678589152294
				],
				[
					0.598923734483992,
					9.583693720513294
				],
				[
					1.7968626003288903,
					9.583693720513294
				],
				[
					1.7968626003288903,
					10.182663153435742
				],
				[
					2.395877731689797,
					10.182663153435742
				],
				[
					2.395877731689797,
					10.182663153435742
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 239,
			"versionNonce": 1156745181,
			"isDeleted": false,
			"id": "orwsxJn0HgnpTZRregw7h",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 828.6783253189685,
			"y": -123.89655147992846,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 30.804604311765388,
			"height": 17.602655016993594,
			"seed": 950393688,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.4668646025420458,
					0
				],
				[
					1.4668646025420458,
					-0.7334323012710229
				],
				[
					2.2003528611107868,
					-0.7334323012710229
				],
				[
					3.6672174636528325,
					-2.2003248824619845
				],
				[
					4.4007057222215735,
					-2.2003248824619845
				],
				[
					5.867570324763847,
					-2.9337851623818665
				],
				[
					6.601058583332588,
					-3.6672174636528894
				],
				[
					7.334434927305892,
					-3.6672174636528894
				],
				[
					8.801299529847938,
					-5.134110044843851
				],
				[
					9.53478778841668,
					-5.134110044843851
				],
				[
					11.001652390958725,
					-5.867542346114874
				],
				[
					11.735140649527466,
					-5.867542346114874
				],
				[
					12.46851699350077,
					-7.334434927305836
				],
				[
					13.93549351063848,
					-8.067867228576858
				],
				[
					14.668869854611785,
					-8.067867228576858
				],
				[
					16.86922271572257,
					-9.53475980976782
				],
				[
					19.06957557683336,
					-10.268220089687702
				],
				[
					21.269928437944145,
					-11.001652390958782
				],
				[
					22.00330478191745,
					-12.468544972149687
				],
				[
					23.470169384459723,
					-13.201977273420766
				],
				[
					24.203657643028464,
					-13.201977273420766
				],
				[
					25.67052224557051,
					-14.668869854611671
				],
				[
					26.40401050413925,
					-14.668869854611671
				],
				[
					27.137386848112556,
					-15.40230215588275
				],
				[
					28.604363365250038,
					-15.40230215588275
				],
				[
					28.604363365250038,
					-16.869194737073713
				],
				[
					29.337739709223342,
					-16.869194737073713
				],
				[
					30.804604311765388,
					-16.869194737073713
				],
				[
					30.804604311765388,
					-17.602655016993594
				],
				[
					30.804604311765388,
					-17.602655016993594
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 226,
			"versionNonce": 524300403,
			"isDeleted": false,
			"id": "eXio_s3O8sTSrQY83ZLsg",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 853.6154712205657,
			"y": -143.69953137938404,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 8.067811271279197,
			"height": 9.534759809767877,
			"seed": 215087656,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7333763439733048,
					0
				],
				[
					1.4668646025420458,
					0
				],
				[
					2.9337292050840915,
					0
				],
				[
					3.6672174636528325,
					0
				],
				[
					5.134082066194878,
					1.4668925811909617
				],
				[
					5.867458410168183,
					1.4668925811909617
				],
				[
					5.867458410168183,
					2.2003248824619845
				],
				[
					7.334434927305892,
					2.2003248824619845
				],
				[
					8.067811271279197,
					2.2003248824619845
				],
				[
					8.067811271279197,
					3.667217463652946
				],
				[
					8.067811271279197,
					4.400677743572828
				],
				[
					8.067811271279197,
					5.134110044843908
				],
				[
					8.067811271279197,
					6.601002626034813
				],
				[
					8.067811271279197,
					7.334434927305892
				],
				[
					6.600946668737151,
					7.334434927305892
				],
				[
					6.600946668737151,
					8.801327508496797
				],
				[
					6.600946668737151,
					9.534759809767877
				],
				[
					6.600946668737151,
					9.534759809767877
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 239,
			"versionNonce": 409961533,
			"isDeleted": false,
			"id": "U6Kzw9k7",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 867.392153579061,
			"y": -154.70118377034282,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 62.01594543457031,
			"height": 40,
			"seed": 1592415784,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Program\nOver",
			"rawText": "Program\nOver",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Program\nOver",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 324,
			"versionNonce": 191343123,
			"isDeleted": false,
			"id": "LyGcLhlW",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 859.3657266518903,
			"y": -35.73778436552748,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 109.9930419921875,
			"height": 53.25353332318113,
			"seed": 279046744,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 14.200942219514967,
			"fontFamily": 1,
			"text": "// This diagram\nis known as \nRecursive Tree",
			"rawText": "// This diagram\nis known as \nRecursive Tree",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "// This diagram\nis known as \nRecursive Tree",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1430,
			"versionNonce": 2144203933,
			"isDeleted": false,
			"id": "ZOiXcV6hKfcAkEtWfWqsC",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 228.47135282775213,
			"y": 222.65724602465713,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 810.7795986610721,
			"height": 542.2523373967291,
			"seed": 1525569112,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 1201,
			"versionNonce": 598667187,
			"isDeleted": false,
			"id": "DNKZSKoz",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 373.8368136616673,
			"y": 257.1169742862014,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 447.0478210449219,
			"height": 35,
			"seed": 296321368,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Fibonacci numbers using recursion",
			"rawText": "Fibonacci numbers using recursion",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibonacci numbers using recursion",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1188,
			"versionNonce": 1723816189,
			"isDeleted": false,
			"id": "4Ok8i-twfCzXmuk1lKqAf",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 539.1740465197415,
			"y": 304.74142791457786,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 478.21880471617715,
			"height": 281.55933191300136,
			"seed": 1051409240,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 721,
			"versionNonce": 1782350163,
			"isDeleted": false,
			"id": "WqlkSe2X",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 777.0168041860634,
			"y": 319.96862943298163,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 40.4539794921875,
			"height": 15.680078905039974,
			"seed": 1117020504,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.544063124031979,
			"fontFamily": 1,
			"text": "Fibo(5)",
			"rawText": "Fibo(5)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(5)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 823,
			"versionNonce": 1187328349,
			"isDeleted": false,
			"id": "UX7QwdfA",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 653.9510360071805,
			"y": 391.3934096316473,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 40.7298583984375,
			"height": 15.680078905039975,
			"seed": 880926296,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.54406312403198,
			"fontFamily": 1,
			"text": "Fibo(4)",
			"rawText": "Fibo(4)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(4)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 811,
			"versionNonce": 1483136755,
			"isDeleted": false,
			"id": "kXZteN4C",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 751.2946942420876,
			"y": 492.1432458909882,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 41.331787109375,
			"height": 15.680078905039975,
			"seed": 196697432,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.54406312403198,
			"fontFamily": 1,
			"text": "Fibo(0)",
			"rawText": "Fibo(0)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(0)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 881,
			"versionNonce": 1831927229,
			"isDeleted": false,
			"id": "NyBxbw9W",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 712.4624162703924,
			"y": 442.4983478360775,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 41.63273620605469,
			"height": 15.680078905039977,
			"seed": 2139962456,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.544063124031982,
			"fontFamily": 1,
			"text": "Fibo(2)",
			"rawText": "Fibo(2)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(2)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 931,
			"versionNonce": 2025097363,
			"isDeleted": false,
			"id": "fV5D8vUn",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 590.3936167468194,
			"y": 443.3327656194708,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 41.24400329589844,
			"height": 15.680078905039975,
			"seed": 1020885848,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.54406312403198,
			"fontFamily": 1,
			"text": "Fibo(3)",
			"rawText": "Fibo(3)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(3)",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 705,
			"versionNonce": 19152413,
			"isDeleted": false,
			"id": "4HZgKy-bh-niTZeQPcTZI",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 691.8632705954759,
			"y": 406.7427635347299,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 35.04338255977292,
			"height": 30.03719414511094,
			"seed": 733624104,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.8343541262537454
				],
				[
					0.8343541262537008,
					-0.8343541262537454
				],
				[
					1.6687082525075796,
					0
				],
				[
					3.3374801621544448,
					0.8343541262537454
				],
				[
					4.171834288408146,
					2.5030942073309683
				],
				[
					4.171834288408146,
					3.337480162154401
				],
				[
					5.006188414662025,
					3.337480162154401
				],
				[
					5.006188414662025,
					4.17183428840819
				],
				[
					6.674896667169427,
					5.840574369485369
				],
				[
					7.5093144505625915,
					6.674928495739159
				],
				[
					9.178022703070171,
					8.34366857681638
				],
				[
					10.012376829323873,
					9.17802270307008
				],
				[
					11.681085081831453,
					10.846762784147305
				],
				[
					12.515502865224615,
					10.846762784147305
				],
				[
					12.515502865224615,
					11.681148738970737
				],
				[
					13.349920648617779,
					11.681148738970737
				],
				[
					13.349920648617779,
					12.515502865224526
				],
				[
					15.018628901125183,
					12.515502865224526
				],
				[
					15.852919370239599,
					14.184242946301747
				],
				[
					15.852919370239599,
					15.01859707255545
				],
				[
					17.52175493702593,
					15.01859707255545
				],
				[
					18.356045406140165,
					16.68733715363267
				],
				[
					19.19046318953333,
					16.68733715363267
				],
				[
					19.19046318953333,
					17.52169127988646
				],
				[
					20.85917144204091,
					17.52169127988646
				],
				[
					21.693589225434074,
					19.190431360963682
				],
				[
					23.362297477941652,
					20.024817315787118
				],
				[
					24.19658794705589,
					20.859171442040907
				],
				[
					25.86542351384222,
					22.52791152311804
				],
				[
					26.699713982956634,
					22.52791152311804
				],
				[
					27.5341317663498,
					23.362265649371828
				],
				[
					29.202840018857202,
					25.031005730449053
				],
				[
					30.037257802250366,
					25.865359856702753
				],
				[
					31.705966054757948,
					26.699745811526274
				],
				[
					32.54025652387218,
					28.368485892603495
				],
				[
					34.20909209065851,
					28.368485892603495
				],
				[
					34.20909209065851,
					29.2028400188572
				],
				[
					35.04338255977292,
					29.2028400188572
				],
				[
					35.04338255977292,
					29.2028400188572
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 705,
			"versionNonce": 1088159283,
			"isDeleted": false,
			"id": "t_VN1D6x8CHyOpKgpD6ap",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 660.1573045407181,
			"y": 405.90840940847613,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 30.87154827136478,
			"height": 30.03719414511094,
			"seed": 1554762280,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.6687082525075794,
					0
				],
				[
					-2.50306237876128,
					0
				],
				[
					-4.171834288408324,
					1.6687082525074908
				],
				[
					-5.006188414662024,
					2.5030942073309683
				],
				[
					-5.840542540915726,
					2.5030942073309683
				],
				[
					-7.509314450562591,
					4.171834288408146
				],
				[
					-8.34366857681647,
					5.006188414661937
				],
				[
					-10.012376829323873,
					6.674928495739113
				],
				[
					-10.84673095557775,
					7.509282621992903
				],
				[
					-12.515502865224615,
					8.343668576816334
				],
				[
					-13.349856991478317,
					10.012376829323825
				],
				[
					-13.349856991478317,
					10.84676278414726
				],
				[
					-14.184211117732017,
					10.84676278414726
				],
				[
					-14.184211117732017,
					12.51550286522448
				],
				[
					-15.852983027379059,
					12.51550286522448
				],
				[
					-16.68733715363276,
					13.349856991478273
				],
				[
					-18.356045406140343,
					15.018597072555492
				],
				[
					-19.19039953239404,
					15.852951198809194
				],
				[
					-20.859171442040907,
					16.687337153632715
				],
				[
					-21.69352556829461,
					16.687337153632715
				],
				[
					-21.69352556829461,
					18.356045406140208
				],
				[
					-22.52787969454849,
					19.190431360963643
				],
				[
					-22.52787969454849,
					20.859171442040864
				],
				[
					-24.196651604195353,
					20.859171442040864
				],
				[
					-24.196651604195353,
					21.693525568294653
				],
				[
					-25.031005730449053,
					21.693525568294653
				],
				[
					-26.699713982956634,
					21.693525568294653
				],
				[
					-26.699713982956634,
					22.52787969454835
				],
				[
					-26.699713982956634,
					24.196619775625575
				],
				[
					-27.53406810921033,
					24.196619775625575
				],
				[
					-27.53406810921033,
					25.03100573044901
				],
				[
					-27.53406810921033,
					26.699713982956503
				],
				[
					-27.53406810921033,
					27.53409993778002
				],
				[
					-27.53406810921033,
					29.202840018857245
				],
				[
					-28.368485892603495,
					29.202840018857245
				],
				[
					-28.368485892603495,
					30.03719414511094
				],
				[
					-30.037194145111076,
					30.03719414511094
				],
				[
					-30.87154827136478,
					30.03719414511094
				],
				[
					-30.87154827136478,
					30.03719414511094
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 712,
			"versionNonce": 1234203261,
			"isDeleted": false,
			"id": "ExX0wzs-kgfLAUMDKbINA",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 739.2705499006161,
			"y": 460.6042736713539,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 18.35604540614016,
			"height": 26.699745811526274,
			"seed": 1791229224,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.8343859548234326
				],
				[
					-1.6687082525075794,
					1.6687400810772222
				],
				[
					-2.502998721621817,
					4.171834288408146
				],
				[
					-4.171834288408146,
					5.006220243231668
				],
				[
					-5.00612475752256,
					7.509346279132322
				],
				[
					-6.674833010030141,
					9.178054531639813
				],
				[
					-6.674833010030141,
					10.846762784147305
				],
				[
					-7.509250793423305,
					12.515534693794258
				],
				[
					-8.34366857681647,
					13.349888820047958
				],
				[
					-8.34366857681647,
					15.018597072555538
				],
				[
					-10.012376829323873,
					15.018597072555538
				],
				[
					-10.012376829323873,
					15.853014855948706
				],
				[
					-10.846667298438286,
					16.6873689822024
				],
				[
					-10.846667298438286,
					18.356077234709893
				],
				[
					-12.515502865224615,
					18.356077234709893
				],
				[
					-13.349793334338852,
					18.356077234709893
				],
				[
					-13.349793334338852,
					19.190431360963682
				],
				[
					-13.349793334338852,
					20.85920327061055
				],
				[
					-15.018501586846433,
					21.693557396864342
				],
				[
					-15.852919370239597,
					23.362265649371828
				],
				[
					-15.852919370239597,
					24.196683432764996
				],
				[
					-16.68733715363276,
					24.196683432764996
				],
				[
					-16.68733715363276,
					25.031037559018788
				],
				[
					-18.35604540614016,
					25.031037559018788
				],
				[
					-18.35604540614016,
					26.699745811526274
				],
				[
					-17.521627622747,
					26.699745811526274
				],
				[
					-17.521627622747,
					26.699745811526274
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 703,
			"versionNonce": 734248915,
			"isDeleted": false,
			"id": "2ritRKvJ3QFNDTNYRxYWc",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 750.2689506331903,
			"y": 460.1422551577823,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 25.031005730449053,
			"height": 30.871580099934423,
			"seed": 1331874856,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.6687082525075794,
					0
				],
				[
					2.5031260359007446,
					0
				],
				[
					2.5031260359007446,
					1.6687082525074908
				],
				[
					4.171834288408146,
					1.6687082525074908
				],
				[
					5.006252071801311,
					2.503094207331012
				],
				[
					5.006252071801311,
					4.171802459838503
				],
				[
					5.840542540915726,
					5.006220243231668
				],
				[
					7.509250793423305,
					6.674928495739159
				],
				[
					8.34366857681647,
					7.509282621992948
				],
				[
					8.34366857681647,
					8.343636748246649
				],
				[
					10.012376829323873,
					10.012408657893603
				],
				[
					10.012376829323873,
					10.846762784147305
				],
				[
					10.846794612717037,
					12.515471036654883
				],
				[
					10.846794612717037,
					13.349888820048049
				],
				[
					12.515502865224615,
					13.349888820048049
				],
				[
					12.515502865224615,
					14.184242946301747
				],
				[
					13.349920648617777,
					15.852951198809238
				],
				[
					14.184211117732017,
					16.687305325063026
				],
				[
					14.184211117732017,
					18.356077234709893
				],
				[
					14.184211117732017,
					19.190431360963682
				],
				[
					15.852919370239597,
					20.859139613471175
				],
				[
					16.68733715363276,
					21.693557396864342
				],
				[
					16.68733715363276,
					22.527911523118128
				],
				[
					18.35604540614016,
					22.527911523118128
				],
				[
					19.19046318953333,
					24.196619775625617
				],
				[
					19.19046318953333,
					25.03097390187932
				],
				[
					20.024753658647747,
					25.03097390187932
				],
				[
					20.024753658647747,
					26.699745811526274
				],
				[
					20.024753658647747,
					27.534099937780063
				],
				[
					21.693589225434074,
					27.534099937780063
				],
				[
					21.693589225434074,
					29.202808190287556
				],
				[
					22.52787969454849,
					29.202808190287556
				],
				[
					22.52787969454849,
					30.03722597368072
				],
				[
					24.19658794705589,
					30.03722597368072
				],
				[
					24.19658794705589,
					30.871580099934423
				],
				[
					25.031005730449053,
					30.871580099934423
				],
				[
					25.031005730449053,
					30.871580099934423
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 1043,
			"versionNonce": 859249373,
			"isDeleted": false,
			"id": "HuFvZxkG",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 547.7740621105028,
			"y": 546.5495281844388,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 36.10260009765625,
			"height": 15.680078905039975,
			"seed": 235601960,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.54406312403198,
			"fontFamily": 1,
			"text": "Fibo(1)",
			"rawText": "Fibo(1)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(1)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1157,
			"versionNonce": 327306611,
			"isDeleted": false,
			"id": "TOamhdZm",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 610.6419538858177,
			"y": 550.7213306442771,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 41.331787109375,
			"height": 15.680078905039975,
			"seed": 1208531752,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.54406312403198,
			"fontFamily": 1,
			"text": "Fibo(0)",
			"rawText": "Fibo(0)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(0)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1227,
			"versionNonce": 380221245,
			"isDeleted": false,
			"id": "ZEE8NWeo",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 571.8096759141226,
			"y": 501.0764325893665,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 41.63273620605469,
			"height": 15.680078905039977,
			"seed": 278337064,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.544063124031982,
			"fontFamily": 1,
			"text": "Fibo(2)",
			"rawText": "Fibo(2)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(2)",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 1039,
			"versionNonce": 1264461587,
			"isDeleted": false,
			"id": "eQ4COt4pCnLUwUevwCUrG",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 592.0944553398946,
			"y": 516.2172138751705,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 18.35604540614016,
			"height": 26.699745811526274,
			"seed": 211947816,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.8343859548234326
				],
				[
					-1.6687082525075794,
					1.6687400810772222
				],
				[
					-2.502998721621817,
					4.171834288408146
				],
				[
					-4.171834288408146,
					5.006220243231668
				],
				[
					-5.00612475752256,
					7.509346279132322
				],
				[
					-6.674833010030141,
					9.178054531639813
				],
				[
					-6.674833010030141,
					10.846762784147305
				],
				[
					-7.509250793423305,
					12.515534693794258
				],
				[
					-8.34366857681647,
					13.349888820047958
				],
				[
					-8.34366857681647,
					15.018597072555538
				],
				[
					-10.012376829323873,
					15.018597072555538
				],
				[
					-10.012376829323873,
					15.853014855948706
				],
				[
					-10.846667298438286,
					16.6873689822024
				],
				[
					-10.846667298438286,
					18.356077234709893
				],
				[
					-12.515502865224615,
					18.356077234709893
				],
				[
					-13.349793334338852,
					18.356077234709893
				],
				[
					-13.349793334338852,
					19.190431360963682
				],
				[
					-13.349793334338852,
					20.85920327061055
				],
				[
					-15.018501586846433,
					21.693557396864342
				],
				[
					-15.852919370239597,
					23.362265649371828
				],
				[
					-15.852919370239597,
					24.196683432764996
				],
				[
					-16.68733715363276,
					24.196683432764996
				],
				[
					-16.68733715363276,
					25.031037559018788
				],
				[
					-18.35604540614016,
					25.031037559018788
				],
				[
					-18.35604540614016,
					26.699745811526274
				],
				[
					-17.521627622747,
					26.699745811526274
				],
				[
					-17.521627622747,
					26.699745811526274
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 1049,
			"versionNonce": 1045022621,
			"isDeleted": false,
			"id": "c10Vo08vTXxnCq4S5D913",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 609.6162102769205,
			"y": 518.7203399110712,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 25.031005730449053,
			"height": 30.871580099934423,
			"seed": 1670753320,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.6687082525075794,
					0
				],
				[
					2.5031260359007446,
					0
				],
				[
					2.5031260359007446,
					1.6687082525074908
				],
				[
					4.171834288408146,
					1.6687082525074908
				],
				[
					5.006252071801311,
					2.503094207331012
				],
				[
					5.006252071801311,
					4.171802459838503
				],
				[
					5.840542540915726,
					5.006220243231668
				],
				[
					7.509250793423305,
					6.674928495739159
				],
				[
					8.34366857681647,
					7.509282621992948
				],
				[
					8.34366857681647,
					8.343636748246649
				],
				[
					10.012376829323873,
					10.012408657893603
				],
				[
					10.012376829323873,
					10.846762784147305
				],
				[
					10.846794612717037,
					12.515471036654883
				],
				[
					10.846794612717037,
					13.349888820048049
				],
				[
					12.515502865224615,
					13.349888820048049
				],
				[
					12.515502865224615,
					14.184242946301747
				],
				[
					13.349920648617777,
					15.852951198809238
				],
				[
					14.184211117732017,
					16.687305325063026
				],
				[
					14.184211117732017,
					18.356077234709893
				],
				[
					14.184211117732017,
					19.190431360963682
				],
				[
					15.852919370239597,
					20.859139613471175
				],
				[
					16.68733715363276,
					21.693557396864342
				],
				[
					16.68733715363276,
					22.527911523118128
				],
				[
					18.35604540614016,
					22.527911523118128
				],
				[
					19.19046318953333,
					24.196619775625617
				],
				[
					19.19046318953333,
					25.03097390187932
				],
				[
					20.024753658647747,
					25.03097390187932
				],
				[
					20.024753658647747,
					26.699745811526274
				],
				[
					20.024753658647747,
					27.534099937780063
				],
				[
					21.693589225434074,
					27.534099937780063
				],
				[
					21.693589225434074,
					29.202808190287556
				],
				[
					22.52787969454849,
					29.202808190287556
				],
				[
					22.52787969454849,
					30.03722597368072
				],
				[
					24.19658794705589,
					30.03722597368072
				],
				[
					24.19658794705589,
					30.871580099934423
				],
				[
					25.031005730449053,
					30.871580099934423
				],
				[
					25.031005730449053,
					30.871580099934423
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 1102,
			"versionNonce": 2043530419,
			"isDeleted": false,
			"id": "8HHPw7A5",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 708.8257518293709,
			"y": 492.39273915888043,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 36.10260009765625,
			"height": 15.680078905039975,
			"seed": 370276184,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.54406312403198,
			"fontFamily": 1,
			"text": "Fibo(1)",
			"rawText": "Fibo(1)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(1)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1232,
			"versionNonce": 742968317,
			"isDeleted": false,
			"id": "MsnKKE0m",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 648.9298862234466,
			"y": 489.5758608857848,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 36.10260009765625,
			"height": 15.680078905039975,
			"seed": 85907752,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.54406312403198,
			"fontFamily": 1,
			"text": "Fibo(1)",
			"rawText": "Fibo(1)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(1)",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 860,
			"versionNonce": 846708307,
			"isDeleted": false,
			"id": "Flcx6fCIkwk2U1vG61RXD",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 616.9947455966859,
			"y": 461.98238677649726,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 24.31417625677069,
			"height": 38.54687914314124,
			"seed": 867620904,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.5930651055066104
				],
				[
					-0.5930198609914704,
					1.1860849664980808
				],
				[
					-1.1860397219829408,
					2.372124688480933
				],
				[
					-1.1860397219829408,
					2.965144549472403
				],
				[
					-2.372079443965792,
					4.744249376961866
				],
				[
					-2.9651445494724022,
					5.337269237953336
				],
				[
					-4.151184271455343,
					6.523354204451507
				],
				[
					-4.744204132446724,
					7.116374065442888
				],
				[
					-5.337223993438195,
					8.89543364841721
				],
				[
					-6.5233089599362755,
					9.48849875392391
				],
				[
					-6.5233089599362755,
					10.674538475906672
				],
				[
					-7.116328820927745,
					10.674538475906672
				],
				[
					-7.116328820927745,
					11.267558336898142
				],
				[
					-8.302368542910598,
					11.267558336898142
				],
				[
					-8.302368542910598,
					12.453643303396312
				],
				[
					-8.895433648417207,
					13.046663164387695
				],
				[
					-9.488453509408677,
					14.232702886370545
				],
				[
					-10.674493231391528,
					14.825722747362017
				],
				[
					-10.674493231391528,
					15.418787852868716
				],
				[
					-11.267513092382998,
					16.604827574851477
				],
				[
					-12.45359805888108,
					17.19784743584295
				],
				[
					-12.45359805888108,
					18.38393240234112
				],
				[
					-13.046617919872551,
					18.9769522633325
				],
				[
					-14.232657641855402,
					19.569972124323883
				],
				[
					-14.825722747362011,
					20.75601184630682
				],
				[
					-14.825722747362011,
					21.349076951813522
				],
				[
					-15.418742608353483,
					22.535116673796285
				],
				[
					-15.418742608353483,
					23.128136534787757
				],
				[
					-16.604782330336334,
					24.314221501285925
				],
				[
					-16.604782330336334,
					24.907241362277308
				],
				[
					-17.197802191327806,
					24.907241362277308
				],
				[
					-17.197802191327806,
					25.50026122326878
				],
				[
					-18.383887157825885,
					25.50026122326878
				],
				[
					-18.383887157825885,
					26.68630094525163
				],
				[
					-18.383887157825885,
					27.27936605075833
				],
				[
					-18.383887157825885,
					28.465405772741182
				],
				[
					-18.976907018817354,
					29.05842563373256
				],
				[
					-18.976907018817354,
					30.244510600230733
				],
				[
					-20.162946740800205,
					30.837530461222112
				],
				[
					-20.756011846306905,
					31.430550322213584
				],
				[
					-20.756011846306905,
					32.616590044196435
				],
				[
					-20.756011846306905,
					33.20965514970314
				],
				[
					-21.34903170729829,
					34.39569487168599
				],
				[
					-22.535071429281142,
					34.988714732677366
				],
				[
					-22.535071429281142,
					35.58173459366884
				],
				[
					-23.12809129027261,
					36.767819560167005
				],
				[
					-23.12809129027261,
					37.36083942115839
				],
				[
					-24.31417625677069,
					37.36083942115839
				],
				[
					-24.31417625677069,
					38.54687914314124
				],
				[
					-24.31417625677069,
					38.54687914314124
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 856,
			"versionNonce": 547898461,
			"isDeleted": false,
			"id": "4uxY0-I7EPPftvYcxYWmK",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 626.4832443506098,
			"y": 461.98238677649726,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 26.686300945251716,
			"height": 27.279366050758327,
			"seed": 1830370344,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.5930198609914705,
					0.5930651055066103
				],
				[
					1.186039721982941,
					1.1860849664980808
				],
				[
					1.779059582974322,
					1.1860849664980808
				],
				[
					1.779059582974322,
					2.372124688480933
				],
				[
					2.9651445494724027,
					2.372124688480933
				],
				[
					2.9651445494724027,
					2.9651445494724027
				],
				[
					3.558164410463873,
					3.5582096549790134
				],
				[
					4.744204132446725,
					4.744249376961866
				],
				[
					5.3372239934381955,
					5.337269237953335
				],
				[
					6.523308959936277,
					6.523354204451506
				],
				[
					6.523308959936277,
					7.116374065442887
				],
				[
					7.116328820927746,
					7.116374065442887
				],
				[
					7.709348681919129,
					8.302413787425737
				],
				[
					8.895433648417299,
					8.895433648417209
				],
				[
					8.895433648417299,
					9.488498753923908
				],
				[
					9.488453509408679,
					9.488498753923908
				],
				[
					9.488453509408679,
					10.67453847590667
				],
				[
					10.67449323139153,
					10.67453847590667
				],
				[
					10.67449323139153,
					11.26755833689814
				],
				[
					11.267513092383,
					12.45364330339631
				],
				[
					12.453598058881083,
					13.046663164387693
				],
				[
					13.046617919872554,
					14.232702886370543
				],
				[
					13.639637780863934,
					14.825722747362015
				],
				[
					14.825722747362102,
					15.418787852868714
				],
				[
					15.418742608353485,
					16.604827574851473
				],
				[
					15.418742608353485,
					17.197847435842945
				],
				[
					16.604782330336427,
					17.197847435842945
				],
				[
					17.19780219132781,
					18.38393240234112
				],
				[
					18.38388715782589,
					18.38393240234112
				],
				[
					18.38388715782589,
					18.9769522633325
				],
				[
					18.976907018817357,
					18.9769522633325
				],
				[
					18.976907018817357,
					19.569972124323883
				],
				[
					19.56992687980883,
					20.75601184630682
				],
				[
					20.75601184630691,
					20.75601184630682
				],
				[
					20.75601184630691,
					21.34907695181352
				],
				[
					21.349031707298295,
					21.34907695181352
				],
				[
					21.349031707298295,
					22.53511667379628
				],
				[
					22.53507142928123,
					22.53511667379628
				],
				[
					22.53507142928123,
					23.128136534787753
				],
				[
					23.12809129027261,
					24.314221501285925
				],
				[
					23.721156395779314,
					24.907241362277304
				],
				[
					23.721156395779314,
					25.500261223268776
				],
				[
					24.907196117762165,
					25.500261223268776
				],
				[
					24.907196117762165,
					26.686300945251627
				],
				[
					25.500215978753634,
					26.686300945251627
				],
				[
					25.500215978753634,
					27.279366050758327
				],
				[
					26.686300945251716,
					27.279366050758327
				],
				[
					26.686300945251716,
					27.279366050758327
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 760,
			"versionNonce": 1345485811,
			"isDeleted": false,
			"id": "cgzhLDjlqdM0EMmDsNOHa",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 783.6358602281322,
			"y": 336.2602759766733,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 96.66368516609131,
			"height": 45.070188103077555,
			"seed": 2016305704,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.1860397219828518,
					0
				],
				[
					-1.779014338459093,
					0.5930198609914258
				],
				[
					-3.558119165948644,
					1.1860623442405107
				],
				[
					-4.151184271455344,
					1.1860623442405107
				],
				[
					-5.3372239934381955,
					2.3721020662233623
				],
				[
					-5.930289098944805,
					2.965144549472447
				],
				[
					-7.709303437403898,
					4.151206893712913
				],
				[
					-9.48840826489345,
					4.744226754704339
				],
				[
					-10.081473370400149,
					4.744226754704339
				],
				[
					-11.267513092383,
					5.337246615695765
				],
				[
					-13.046617919872554,
					5.337246615695765
				],
				[
					-13.639592536348706,
					6.523308959936276
				],
				[
					-15.418697363838257,
					7.116351443185317
				],
				[
					-16.01176246934496,
					7.116351443185317
				],
				[
					-17.790867296834417,
					8.302391165168167
				],
				[
					-19.569881635293513,
					8.895433648417209
				],
				[
					-21.34898646278306,
					10.08149599265772
				],
				[
					-23.12809129027261,
					10.674515853649146
				],
				[
					-24.907196117762165,
					11.26753571464057
				],
				[
					-26.093235839745017,
					12.45359805888108
				],
				[
					-27.279275561727868,
					13.046640542130122
				],
				[
					-29.65144549472412,
					14.232680264112972
				],
				[
					-30.83748521670697,
					14.232680264112972
				],
				[
					-33.209564660672676,
					14.825722747362057
				],
				[
					-33.80262976617937,
					16.011785091602523
				],
				[
					-35.581734593668926,
					16.60480495259395
				],
				[
					-37.36074893212802,
					16.60480495259395
				],
				[
					-37.95381403763462,
					17.19782481358542
				],
				[
					-39.13985375961757,
					17.19782481358542
				],
				[
					-40.918958587107035,
					18.38388715782589
				],
				[
					-41.51202369261373,
					18.38388715782589
				],
				[
					-42.10499830908997,
					18.38388715782589
				],
				[
					-42.10499830908997,
					18.976929641074925
				],
				[
					-43.29103803107282,
					18.976929641074925
				],
				[
					-45.07014285856238,
					20.162969363057822
				],
				[
					-45.66320796406898,
					20.162969363057822
				],
				[
					-46.84924768605183,
					20.162969363057822
				],
				[
					-47.44231279155853,
					20.756011846306862
				],
				[
					-48.035287408034776,
					20.756011846306862
				],
				[
					-49.22132713001762,
					21.94207419054733
				],
				[
					-49.81439223552424,
					21.94207419054733
				],
				[
					-51.59349706301379,
					22.535094051538756
				],
				[
					-53.37260189050335,
					23.128113912530225
				],
				[
					-53.96557650697959,
					23.128113912530225
				],
				[
					-55.744681334469135,
					24.31417625677069
				],
				[
					-56.93072105645199,
					24.31417625677069
				],
				[
					-57.5237861619586,
					24.90721874001973
				],
				[
					-58.70982588394154,
					24.90721874001973
				],
				[
					-59.302890989448144,
					26.093258462002627
				],
				[
					-59.895865605924385,
					26.093258462002627
				],
				[
					-61.081905327907236,
					26.68630094525167
				],
				[
					-61.67497043341394,
					26.68630094525167
				],
				[
					-62.861010155396784,
					27.279320806243092
				],
				[
					-63.4540752609034,
					27.279320806243092
				],
				[
					-64.04704987737965,
					28.465383150483607
				],
				[
					-65.23318008839296,
					28.465383150483607
				],
				[
					-65.8261547048692,
					29.05840301147503
				],
				[
					-67.01219442685205,
					29.05840301147503
				],
				[
					-67.60525953235874,
					30.244465355715494
				],
				[
					-68.7912992543416,
					30.244465355715494
				],
				[
					-69.97733897632446,
					30.837507838964537
				],
				[
					-71.16346918733775,
					32.023547560947435
				],
				[
					-71.756443803814,
					32.023547560947435
				],
				[
					-72.94252877031208,
					32.61659004419647
				],
				[
					-74.72163359780163,
					32.61659004419647
				],
				[
					-74.72163359780163,
					33.2096099051879
				],
				[
					-75.3146534587931,
					33.2096099051879
				],
				[
					-75.9076733197845,
					33.2096099051879
				],
				[
					-77.09371304176733,
					34.39567224942841
				],
				[
					-77.68677814727404,
					34.39567224942841
				],
				[
					-78.87281786925689,
					34.39567224942841
				],
				[
					-79.46583773024835,
					34.98869211041984
				],
				[
					-80.05885759123973,
					34.98869211041984
				],
				[
					-81.24494255773791,
					36.1747544546603
				],
				[
					-81.8379624187293,
					36.1747544546603
				],
				[
					-83.02400214071223,
					36.76779693790939
				],
				[
					-83.61706724621885,
					36.76779693790939
				],
				[
					-84.8031069682017,
					37.95383665989224
				],
				[
					-85.39612682919318,
					37.95383665989224
				],
				[
					-85.98914669018464,
					38.54687914314128
				],
				[
					-87.17523165668273,
					38.54687914314128
				],
				[
					-87.17523165668273,
					39.139899004132744
				],
				[
					-87.7682515176741,
					39.139899004132744
				],
				[
					-88.95429123965704,
					39.139899004132744
				],
				[
					-88.95429123965704,
					40.32596134837322
				],
				[
					-89.54735634516365,
					40.32596134837322
				],
				[
					-90.7333960671465,
					40.32596134837322
				],
				[
					-91.32641592813796,
					40.918981209364645
				],
				[
					-91.91943578912944,
					40.918981209364645
				],
				[
					-91.91943578912944,
					42.10504355360516
				],
				[
					-93.10552075562751,
					42.10504355360516
				],
				[
					-93.6985406166189,
					42.698086036854185
				],
				[
					-94.88458033860184,
					43.29110589784562
				],
				[
					-95.47764544410845,
					43.29110589784562
				],
				[
					-95.47764544410845,
					44.47716824208609
				],
				[
					-96.66368516609131,
					44.47716824208609
				],
				[
					-96.66368516609131,
					45.070188103077555
				],
				[
					-96.66368516609131,
					45.070188103077555
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 1059,
			"versionNonce": 1597616317,
			"isDeleted": false,
			"id": "nlUeiZer",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 910.7996828052803,
			"y": 392.59042723102067,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 41.24400329589844,
			"height": 15.680078905039975,
			"seed": 1015061336,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.54406312403198,
			"fontFamily": 1,
			"text": "Fibo(3)",
			"rawText": "Fibo(3)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(3)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1172,
			"versionNonce": 251954579,
			"isDeleted": false,
			"id": "T0yj9shF",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 868.1801281689637,
			"y": 495.8071897959888,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 36.10260009765625,
			"height": 15.680078905039975,
			"seed": 1971548248,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.54406312403198,
			"fontFamily": 1,
			"text": "Fibo(1)",
			"rawText": "Fibo(1)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(1)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1286,
			"versionNonce": 899584285,
			"isDeleted": false,
			"id": "ep74lFcS",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 931.0480199442786,
			"y": 499.97899225582694,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 41.331787109375,
			"height": 15.680078905039975,
			"seed": 291743064,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.54406312403198,
			"fontFamily": 1,
			"text": "Fibo(0)",
			"rawText": "Fibo(0)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(0)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1356,
			"versionNonce": 1713658675,
			"isDeleted": false,
			"id": "4LCBMfXH",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 892.2157419725835,
			"y": 450.33409420091635,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 41.63273620605469,
			"height": 15.680078905039977,
			"seed": 225786456,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"fontSize": 12.544063124031982,
			"fontFamily": 1,
			"text": "Fibo(2)",
			"rawText": "Fibo(2)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(2)",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 1168,
			"versionNonce": 1095263613,
			"isDeleted": false,
			"id": "wKdxX5rVi0ffbs4Jkxcb7",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 912.5005213983554,
			"y": 465.4748754867205,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 18.35604540614016,
			"height": 26.699745811526274,
			"seed": 478949208,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158213,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.8343859548234326
				],
				[
					-1.6687082525075794,
					1.6687400810772222
				],
				[
					-2.502998721621817,
					4.171834288408146
				],
				[
					-4.171834288408146,
					5.006220243231668
				],
				[
					-5.00612475752256,
					7.509346279132322
				],
				[
					-6.674833010030141,
					9.178054531639813
				],
				[
					-6.674833010030141,
					10.846762784147305
				],
				[
					-7.509250793423305,
					12.515534693794258
				],
				[
					-8.34366857681647,
					13.349888820047958
				],
				[
					-8.34366857681647,
					15.018597072555538
				],
				[
					-10.012376829323873,
					15.018597072555538
				],
				[
					-10.012376829323873,
					15.853014855948706
				],
				[
					-10.846667298438286,
					16.6873689822024
				],
				[
					-10.846667298438286,
					18.356077234709893
				],
				[
					-12.515502865224615,
					18.356077234709893
				],
				[
					-13.349793334338852,
					18.356077234709893
				],
				[
					-13.349793334338852,
					19.190431360963682
				],
				[
					-13.349793334338852,
					20.85920327061055
				],
				[
					-15.018501586846433,
					21.693557396864342
				],
				[
					-15.852919370239597,
					23.362265649371828
				],
				[
					-15.852919370239597,
					24.196683432764996
				],
				[
					-16.68733715363276,
					24.196683432764996
				],
				[
					-16.68733715363276,
					25.031037559018788
				],
				[
					-18.35604540614016,
					25.031037559018788
				],
				[
					-18.35604540614016,
					26.699745811526274
				],
				[
					-17.521627622747,
					26.699745811526274
				],
				[
					-17.521627622747,
					26.699745811526274
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 1178,
			"versionNonce": 569933011,
			"isDeleted": false,
			"id": "wilxvaBCzpG17xafguUxq",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 930.0222763353813,
			"y": 467.97800152262107,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 25.031005730449053,
			"height": 30.871580099934423,
			"seed": 1996260440,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.6687082525075794,
					0
				],
				[
					2.5031260359007446,
					0
				],
				[
					2.5031260359007446,
					1.6687082525074908
				],
				[
					4.171834288408146,
					1.6687082525074908
				],
				[
					5.006252071801311,
					2.503094207331012
				],
				[
					5.006252071801311,
					4.171802459838503
				],
				[
					5.840542540915726,
					5.006220243231668
				],
				[
					7.509250793423305,
					6.674928495739159
				],
				[
					8.34366857681647,
					7.509282621992948
				],
				[
					8.34366857681647,
					8.343636748246649
				],
				[
					10.012376829323873,
					10.012408657893603
				],
				[
					10.012376829323873,
					10.846762784147305
				],
				[
					10.846794612717037,
					12.515471036654883
				],
				[
					10.846794612717037,
					13.349888820048049
				],
				[
					12.515502865224615,
					13.349888820048049
				],
				[
					12.515502865224615,
					14.184242946301747
				],
				[
					13.349920648617777,
					15.852951198809238
				],
				[
					14.184211117732017,
					16.687305325063026
				],
				[
					14.184211117732017,
					18.356077234709893
				],
				[
					14.184211117732017,
					19.190431360963682
				],
				[
					15.852919370239597,
					20.859139613471175
				],
				[
					16.68733715363276,
					21.693557396864342
				],
				[
					16.68733715363276,
					22.527911523118128
				],
				[
					18.35604540614016,
					22.527911523118128
				],
				[
					19.19046318953333,
					24.196619775625617
				],
				[
					19.19046318953333,
					25.03097390187932
				],
				[
					20.024753658647747,
					25.03097390187932
				],
				[
					20.024753658647747,
					26.699745811526274
				],
				[
					20.024753658647747,
					27.534099937780063
				],
				[
					21.693589225434074,
					27.534099937780063
				],
				[
					21.693589225434074,
					29.202808190287556
				],
				[
					22.52787969454849,
					29.202808190287556
				],
				[
					22.52787969454849,
					30.03722597368072
				],
				[
					24.19658794705589,
					30.03722597368072
				],
				[
					24.19658794705589,
					30.871580099934423
				],
				[
					25.031005730449053,
					30.871580099934423
				],
				[
					25.031005730449053,
					30.871580099934423
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 1361,
			"versionNonce": 1970843101,
			"isDeleted": false,
			"id": "WC4FbLX7",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 969.3359522819076,
			"y": 438.8335224973346,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 36.10260009765625,
			"height": 15.680078905039975,
			"seed": 714750296,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"fontSize": 12.54406312403198,
			"fontFamily": 1,
			"text": "Fibo(1)",
			"rawText": "Fibo(1)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(1)",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 989,
			"versionNonce": 1041721971,
			"isDeleted": false,
			"id": "4uYsixGuF5-S7OUFUeSNz",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 937.4008116551469,
			"y": 411.24004838804717,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 24.31417625677069,
			"height": 38.54687914314124,
			"seed": 1790529112,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.5930651055066104
				],
				[
					-0.5930198609914704,
					1.1860849664980808
				],
				[
					-1.1860397219829408,
					2.372124688480933
				],
				[
					-1.1860397219829408,
					2.965144549472403
				],
				[
					-2.372079443965792,
					4.744249376961866
				],
				[
					-2.9651445494724022,
					5.337269237953336
				],
				[
					-4.151184271455343,
					6.523354204451507
				],
				[
					-4.744204132446724,
					7.116374065442888
				],
				[
					-5.337223993438195,
					8.89543364841721
				],
				[
					-6.5233089599362755,
					9.48849875392391
				],
				[
					-6.5233089599362755,
					10.674538475906672
				],
				[
					-7.116328820927745,
					10.674538475906672
				],
				[
					-7.116328820927745,
					11.267558336898142
				],
				[
					-8.302368542910598,
					11.267558336898142
				],
				[
					-8.302368542910598,
					12.453643303396312
				],
				[
					-8.895433648417207,
					13.046663164387695
				],
				[
					-9.488453509408677,
					14.232702886370545
				],
				[
					-10.674493231391528,
					14.825722747362017
				],
				[
					-10.674493231391528,
					15.418787852868716
				],
				[
					-11.267513092382998,
					16.604827574851477
				],
				[
					-12.45359805888108,
					17.19784743584295
				],
				[
					-12.45359805888108,
					18.38393240234112
				],
				[
					-13.046617919872551,
					18.9769522633325
				],
				[
					-14.232657641855402,
					19.569972124323883
				],
				[
					-14.825722747362011,
					20.75601184630682
				],
				[
					-14.825722747362011,
					21.349076951813522
				],
				[
					-15.418742608353483,
					22.535116673796285
				],
				[
					-15.418742608353483,
					23.128136534787757
				],
				[
					-16.604782330336334,
					24.314221501285925
				],
				[
					-16.604782330336334,
					24.907241362277308
				],
				[
					-17.197802191327806,
					24.907241362277308
				],
				[
					-17.197802191327806,
					25.50026122326878
				],
				[
					-18.383887157825885,
					25.50026122326878
				],
				[
					-18.383887157825885,
					26.68630094525163
				],
				[
					-18.383887157825885,
					27.27936605075833
				],
				[
					-18.383887157825885,
					28.465405772741182
				],
				[
					-18.976907018817354,
					29.05842563373256
				],
				[
					-18.976907018817354,
					30.244510600230733
				],
				[
					-20.162946740800205,
					30.837530461222112
				],
				[
					-20.756011846306905,
					31.430550322213584
				],
				[
					-20.756011846306905,
					32.616590044196435
				],
				[
					-20.756011846306905,
					33.20965514970314
				],
				[
					-21.34903170729829,
					34.39569487168599
				],
				[
					-22.535071429281142,
					34.988714732677366
				],
				[
					-22.535071429281142,
					35.58173459366884
				],
				[
					-23.12809129027261,
					36.767819560167005
				],
				[
					-23.12809129027261,
					37.36083942115839
				],
				[
					-24.31417625677069,
					37.36083942115839
				],
				[
					-24.31417625677069,
					38.54687914314124
				],
				[
					-24.31417625677069,
					38.54687914314124
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 985,
			"versionNonce": 1631644221,
			"isDeleted": false,
			"id": "YzhUf2ulNo4FdFTLlcAMX",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 946.8893104090706,
			"y": 411.24004838804717,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 26.686300945251716,
			"height": 27.279366050758327,
			"seed": 1613611864,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.5930198609914705,
					0.5930651055066103
				],
				[
					1.186039721982941,
					1.1860849664980808
				],
				[
					1.779059582974322,
					1.1860849664980808
				],
				[
					1.779059582974322,
					2.372124688480933
				],
				[
					2.9651445494724027,
					2.372124688480933
				],
				[
					2.9651445494724027,
					2.9651445494724027
				],
				[
					3.558164410463873,
					3.5582096549790134
				],
				[
					4.744204132446725,
					4.744249376961866
				],
				[
					5.3372239934381955,
					5.337269237953335
				],
				[
					6.523308959936277,
					6.523354204451506
				],
				[
					6.523308959936277,
					7.116374065442887
				],
				[
					7.116328820927746,
					7.116374065442887
				],
				[
					7.709348681919129,
					8.302413787425737
				],
				[
					8.895433648417299,
					8.895433648417209
				],
				[
					8.895433648417299,
					9.488498753923908
				],
				[
					9.488453509408679,
					9.488498753923908
				],
				[
					9.488453509408679,
					10.67453847590667
				],
				[
					10.67449323139153,
					10.67453847590667
				],
				[
					10.67449323139153,
					11.26755833689814
				],
				[
					11.267513092383,
					12.45364330339631
				],
				[
					12.453598058881083,
					13.046663164387693
				],
				[
					13.046617919872554,
					14.232702886370543
				],
				[
					13.639637780863934,
					14.825722747362015
				],
				[
					14.825722747362102,
					15.418787852868714
				],
				[
					15.418742608353485,
					16.604827574851473
				],
				[
					15.418742608353485,
					17.197847435842945
				],
				[
					16.604782330336427,
					17.197847435842945
				],
				[
					17.19780219132781,
					18.38393240234112
				],
				[
					18.38388715782589,
					18.38393240234112
				],
				[
					18.38388715782589,
					18.9769522633325
				],
				[
					18.976907018817357,
					18.9769522633325
				],
				[
					18.976907018817357,
					19.569972124323883
				],
				[
					19.56992687980883,
					20.75601184630682
				],
				[
					20.75601184630691,
					20.75601184630682
				],
				[
					20.75601184630691,
					21.34907695181352
				],
				[
					21.349031707298295,
					21.34907695181352
				],
				[
					21.349031707298295,
					22.53511667379628
				],
				[
					22.53507142928123,
					22.53511667379628
				],
				[
					22.53507142928123,
					23.128136534787753
				],
				[
					23.12809129027261,
					24.314221501285925
				],
				[
					23.721156395779314,
					24.907241362277304
				],
				[
					23.721156395779314,
					25.500261223268776
				],
				[
					24.907196117762165,
					25.500261223268776
				],
				[
					24.907196117762165,
					26.686300945251627
				],
				[
					25.500215978753634,
					26.686300945251627
				],
				[
					25.500215978753634,
					27.279366050758327
				],
				[
					26.686300945251716,
					27.279366050758327
				],
				[
					26.686300945251716,
					27.279366050758327
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 707,
			"versionNonce": 2135401491,
			"isDeleted": false,
			"id": "VedSue17qgqhER3LsUc6N",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 815.0664105503456,
			"y": 338.6323780428967,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 106.7452037810067,
			"height": 52.18656216852045,
			"seed": 1762658392,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.5930651055066993,
					0
				],
				[
					1.186039721982941,
					0
				],
				[
					1.7791048274894619,
					0
				],
				[
					2.9651445494724027,
					1.1860623442404665
				],
				[
					4.744249376961866,
					1.7791048274895513
				],
				[
					5.930289098944805,
					2.372124688480977
				],
				[
					8.895433648417209,
					4.151206893712914
				],
				[
					11.267603581413368,
					5.930289098944805
				],
				[
					14.825722747362015,
					7.709393926434357
				],
				[
					18.38393240234112,
					10.081495992657722
				],
				[
					23.12818177930298,
					11.86057819788961
				],
				[
					29.05847087824779,
					15.4187652306111
				],
				[
					38.54687914314124,
					18.97692964107493
				],
				[
					45.66320796406898,
					22.53511667379637
				],
				[
					52.779627274027185,
					26.686300945251674
				],
				[
					59.89595609495477,
					28.46540577274118
				],
				[
					67.60535002138921,
					33.209632527445514
				],
				[
					74.72167884231676,
					36.17477707691792
				],
				[
					79.4659282192788,
					37.95385928214986
				],
				[
					81.83800766324451,
					39.732941487381794
				],
				[
					83.61711249073399,
					40.32598397063083
				],
				[
					85.39621731822363,
					40.32598397063083
				],
				[
					85.98919193469986,
					41.51202369261369
				],
				[
					87.17523165668264,
					41.51202369261369
				],
				[
					87.17523165668264,
					42.10506617586273
				],
				[
					87.76829676218932,
					42.10506617586273
				],
				[
					88.95433648417226,
					42.69808603685419
				],
				[
					89.5474015896788,
					43.88414838109466
				],
				[
					90.73344131166172,
					43.88414838109466
				],
				[
					91.32650641716843,
					44.477168242086094
				],
				[
					91.91948103364467,
					44.477168242086094
				],
				[
					93.69858586113412,
					45.6632305863266
				],
				[
					95.47769068862358,
					46.256273069575634
				],
				[
					97.25679551611324,
					47.442312791558486
				],
				[
					99.03580985457225,
					48.035355274807586
				],
				[
					99.62887496007893,
					48.628375135799
				],
				[
					100.81491468206188,
					48.628375135799
				],
				[
					101.4079797875684,
					49.814437480039466
				],
				[
					102.00095440404465,
					49.814437480039466
				],
				[
					103.18708461505804,
					49.814437480039466
				],
				[
					103.18708461505804,
					50.40745734103094
				],
				[
					103.78005923153428,
					50.40745734103094
				],
				[
					104.96609895351705,
					50.40745734103094
				],
				[
					104.96609895351705,
					51.5935196852714
				],
				[
					105.55916405902374,
					51.5935196852714
				],
				[
					105.55916405902374,
					52.18656216852045
				],
				[
					106.7452037810067,
					52.18656216852045
				],
				[
					106.7452037810067,
					52.18656216852045
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 547,
			"versionNonce": 897751709,
			"isDeleted": false,
			"id": "CGwrF2pi",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 225.0878399405418,
			"y": 343.1593578757271,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 255.9998321533203,
			"height": 40,
			"seed": 433642792,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# First break the problem down \ninto smaller problems...",
			"rawText": "# First break the problem down \ninto smaller problems...",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# First break the problem down \ninto smaller problems...",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 735,
			"versionNonce": 1300212147,
			"isDeleted": false,
			"id": "bBELOlAN",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 235.26490799034661,
			"y": 412.5943238925707,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 260.21197509765625,
			"height": 23.07935341084301,
			"seed": 235384616,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"fontSize": 18.463482728674407,
			"fontFamily": 1,
			"text": "Fibo(n) = fibo(n-1) + fibo(n-2)",
			"rawText": "Fibo(n) = fibo(n-1) + fibo(n-2)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Fibo(n) = fibo(n-1) + fibo(n-2)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 547,
			"versionNonce": 1334196947,
			"isDeleted": false,
			"id": "65GiPJfv",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 246.16288242608937,
			"y": 457.2713986157083,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 274.1438293457031,
			"height": 60,
			"seed": 1138909016,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421679860,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# When you write recursion in a \nformula it is termed as recurrent \nrelation",
			"rawText": "# When you write recursion in a \nformula it is termed as recurrent \nrelation",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# When you write recursion in a \nformula it is termed as recurrent \nrelation",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 289,
			"versionNonce": 1342375411,
			"isDeleted": false,
			"id": "lEcGNk4Z",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 253.47153928463632,
			"y": 536.1903221410806,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 289.9358215332031,
			"height": 40,
			"seed": 494570024,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421678805,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "-> The base condition is regarded by\nanswers we already have ",
			"rawText": "-> The base condition is regarded by\nanswers we already have ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "-> The base condition is regarded by\nanswers we already have ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 346,
			"versionNonce": 1745377117,
			"isDeleted": false,
			"id": "mSTGfb0Z",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 228.535558054528,
			"y": 636.0251071707332,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 558.65576171875,
			"height": 20,
			"seed": 568571224,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "For Example: In this case we already know that F(0) = 0 and F(1) = 1",
			"rawText": "For Example: In this case we already know that F(0) = 0 and F(1) = 1",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "For Example: In this case we already know that F(0) = 0 and F(1) = 1",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 228,
			"versionNonce": 1020336371,
			"isDeleted": false,
			"id": "yYLFcK_MeF431PM2DZ-bO",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 410.30394832676564,
			"y": 582.1500625507418,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 23.490565155603917,
			"height": 39.83179060592829,
			"seed": 692592216,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-1.0213119804373036
				],
				[
					1.0213899015466268,
					-1.0213119804373036
				],
				[
					3.064013862421234,
					-1.0213119804373036
				],
				[
					4.08532584285831,
					1.0213119804373036
				],
				[
					4.08532584285831,
					2.0426239608744936
				],
				[
					4.08532584285831,
					4.085325842858424
				],
				[
					6.128027724842241,
					6.127949803732918
				],
				[
					6.128027724842241,
					8.170651685716848
				],
				[
					7.149339705279544,
					11.234587627028645
				],
				[
					7.149339705279544,
					12.255899607465949
				],
				[
					7.149339705279544,
					13.277289509012576
				],
				[
					7.149339705279544,
					15.31991346988707
				],
				[
					9.191963666154152,
					16.341225450324373
				],
				[
					9.191963666154152,
					18.38392733230819
				],
				[
					9.191963666154152,
					19.405239312745493
				],
				[
					9.191963666154152,
					21.447863273619987
				],
				[
					9.191963666154152,
					22.46917525405729
				],
				[
					9.191963666154152,
					23.490565155603917
				],
				[
					10.213275646591455,
					23.490565155603917
				],
				[
					10.213275646591455,
					25.53318911647841
				],
				[
					10.213275646591455,
					26.554501096915715
				],
				[
					11.234665548138082,
					26.554501096915715
				],
				[
					11.234665548138082,
					28.597202978899645
				],
				[
					11.234665548138082,
					29.618514959336835
				],
				[
					11.234665548138082,
					31.661138920211442
				],
				[
					13.277289509012462,
					31.661138920211442
				],
				[
					13.277289509012462,
					32.68245090064863
				],
				[
					12.255977528575158,
					32.68245090064863
				],
				[
					11.234665548138082,
					32.68245090064863
				],
				[
					10.213275646591455,
					32.68245090064863
				],
				[
					10.213275646591455,
					30.63982693977414
				],
				[
					8.170651685716848,
					30.63982693977414
				],
				[
					8.170651685716848,
					29.618514959336835
				],
				[
					7.149339705279544,
					29.618514959336835
				],
				[
					5.106637823295614,
					29.618514959336835
				],
				[
					5.106637823295614,
					27.57581307735302
				],
				[
					5.106637823295614,
					28.597202978899645
				],
				[
					6.128027724842241,
					28.597202978899645
				],
				[
					7.149339705279544,
					29.618514959336835
				],
				[
					9.191963666154152,
					31.661138920211442
				],
				[
					10.213275646591455,
					32.68245090064863
				],
				[
					10.213275646591455,
					33.70384080219526
				],
				[
					11.234665548138082,
					33.70384080219526
				],
				[
					11.234665548138082,
					35.746464763069866
				],
				[
					13.277289509012462,
					35.746464763069866
				],
				[
					14.298601489449766,
					36.767776743507056
				],
				[
					16.341303371433696,
					38.81047862549099
				],
				[
					16.341303371433696,
					37.78908872394436
				],
				[
					16.341303371433696,
					36.767776743507056
				],
				[
					16.341303371433696,
					34.72515278263256
				],
				[
					17.362615351871,
					34.72515278263256
				],
				[
					17.362615351871,
					33.70384080219526
				],
				[
					18.383927332308303,
					32.68245090064863
				],
				[
					18.383927332308303,
					30.63982693977414
				],
				[
					20.426551293182683,
					30.63982693977414
				],
				[
					21.44794119472931,
					29.618514959336835
				],
				[
					23.490565155603917,
					27.57581307735302
				],
				[
					23.490565155603917,
					26.554501096915715
				],
				[
					23.490565155603917,
					26.554501096915715
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 579,
			"versionNonce": 1994053779,
			"isDeleted": false,
			"id": "34hy3u6q",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 263.91972541290215,
			"y": 687.119166576753,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 732.4796142578125,
			"height": 60,
			"seed": 529678168,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421675636,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# We were able to identify that this was an question which can be solved with the help of \nrecursion as we knew the base conditions and was able to break the problems into\nmultiple smaller problems.",
			"rawText": "# We were able to identify that this was an question which can be solved with the help of \nrecursion as we knew the base conditions and was able to break the problems into\nmultiple smaller problems.",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# We were able to identify that this was an question which can be solved with the help of \nrecursion as we knew the base conditions and was able to break the problems into\nmultiple smaller problems.",
			"lineHeight": 1.25
		},
		{
			"type": "ellipse",
			"version": 570,
			"versionNonce": 130515603,
			"isDeleted": false,
			"id": "e0ha9T9Z08XOOeUTeYqju",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 917.959574648344,
			"y": 231.2867282925111,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 80.9803541126721,
			"height": 88.58675454088414,
			"seed": 774301016,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "4GId5vda"
				}
			],
			"updated": 1715421158214,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 501,
			"versionNonce": 1549132829,
			"isDeleted": false,
			"id": "4GId5vda",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 949.3588738522282,
			"y": 258.2599581333695,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 17.919998168945312,
			"height": 35,
			"seed": 802191960,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "4",
			"rawText": "4",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "e0ha9T9Z08XOOeUTeYqju",
			"originalText": "4",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 294,
			"versionNonce": 662681651,
			"isDeleted": false,
			"id": "PsEsPDne",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 634.2521267391679,
			"y": 547.6277214305777,
			"strokeColor": "#ff8787",
			"backgroundColor": "transparent",
			"width": 335.5517883300781,
			"height": 20,
			"seed": 580394792,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "fig : Recursive tree for Fibonacci numbers ",
			"rawText": "fig : Recursive tree for Fibonacci numbers ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "fig : Recursive tree for Fibonacci numbers ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 328,
			"versionNonce": 1537038461,
			"isDeleted": false,
			"id": "GnCI0LkM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": -630.749768085243,
			"y": -434.2679233410821,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 797.61572265625,
			"height": 45,
			"seed": 1780534056,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 1,
			"text": "Code Vault path: \"C:\\IDK\\Java\\Recursion\\...\"",
			"rawText": "Code Vault path: \"C:\\IDK\\Java\\Recursion\\...\"",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Code Vault path: \"C:\\IDK\\Java\\Recursion\\...\"",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 264,
			"versionNonce": 970996179,
			"isDeleted": false,
			"id": "PP5AjEBg4JdnLVCa_EK_B",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 772.3691878901241,
			"y": 322.23565172890517,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 108.74384670068935,
			"height": 60.83197946644265,
			"seed": 1936848680,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-3.7683352638932774,
					0
				],
				[
					-4.306704077398649,
					0
				],
				[
					-5.383359560861322,
					0
				],
				[
					-6.460015044323995,
					0
				],
				[
					-9.151694824754713,
					0
				],
				[
					-10.766719121722645,
					0
				],
				[
					-11.30500579168006,
					0.5383482776183541
				],
				[
					-13.458398902153363,
					0.5383482776183541
				],
				[
					-15.073423199121407,
					1.0766760193496907
				],
				[
					-16.68836535254127,
					1.0766760193496907
				],
				[
					-18.303389649509313,
					1.0766760193496907
				],
				[
					-18.841758463014685,
					1.0766760193496907
				],
				[
					-20.456782759982616,
					1.0766760193496907
				],
				[
					-20.99506942994003,
					2.1533520386993814
				],
				[
					-22.071724913402704,
					2.1533520386993814
				],
				[
					-22.610093726907962,
					2.1533520386993814
				],
				[
					-24.225118023876007,
					2.691679780430718
				],
				[
					-25.30177350733868,
					2.691679780430718
				],
				[
					-25.840142320844052,
					2.691679780430718
				],
				[
					-27.455084474264027,
					2.691679780430718
				],
				[
					-27.9934532877694,
					3.2300280580490153
				],
				[
					-29.60847758473733,
					3.2300280580490153
				],
				[
					-31.22350188170526,
					3.2300280580490153
				],
				[
					-32.83844403512535,
					4.306704077398649
				],
				[
					-36.068492629061325,
					4.306704077398649
				],
				[
					-38.22180359598667,
					4.306704077398649
				],
				[
					-39.836827892954716,
					4.845031819129986
				],
				[
					-41.990221003427905,
					5.921707838479676
				],
				[
					-43.60516315684799,
					5.921707838479676
				],
				[
					-45.220187453815925,
					6.460035580211013
				],
				[
					-46.83521175078397,
					6.460035580211013
				],
				[
					-47.91186723424664,
					6.460035580211013
				],
				[
					-50.60354701467736,
					7.536711599560704
				],
				[
					-52.21857131164529,
					7.536711599560704
				],
				[
					-53.295226795107965,
					8.07503934129204
				],
				[
					-54.910251092075896,
					8.07503934129204
				],
				[
					-57.601930872506614,
					8.613387618910338
				],
				[
					-58.67858635596929,
					8.613387618910338
				],
				[
					-60.29361065293733,
					9.690063638260028
				],
				[
					-61.90863494990526,
					10.228391379991365
				],
				[
					-64.06198698860464,
					10.228391379991365
				],
				[
					-65.67697021379865,
					10.228391379991365
				],
				[
					-67.2919945107667,
					11.305067399341056
				],
				[
					-68.90697773596071,
					11.843395141072392
				],
				[
					-70.52200203292864,
					12.920071160422026
				],
				[
					-72.13702632989657,
					12.920071160422026
				],
				[
					-72.67535407162791,
					13.458398902153363
				],
				[
					-74.29033729682192,
					13.458398902153363
				],
				[
					-74.82870611032729,
					13.99674717977166
				],
				[
					-75.90536159378996,
					13.99674717977166
				],
				[
					-76.4436893355213,
					13.99674717977166
				],
				[
					-76.98201707725264,
					15.07342319912135
				],
				[
					-78.05871363248934,
					15.611750940852687
				],
				[
					-78.59704137422068,
					15.611750940852687
				],
				[
					-79.67369685768335,
					15.611750940852687
				],
				[
					-79.67369685768335,
					16.688426960202378
				],
				[
					-80.21206567118861,
					17.226754701933714
				],
				[
					-81.28872115465128,
					17.226754701933714
				],
				[
					-81.82704889638262,
					18.30343072128335
				],
				[
					-82.36537663811396,
					18.30343072128335
				],
				[
					-83.44207319335055,
					18.841758463014685
				],
				[
					-85.05705641854456,
					19.380106740632982
				],
				[
					-85.59542523204993,
					20.456782759982673
				],
				[
					-86.6720807155126,
					20.99511050171401
				],
				[
					-86.6720807155126,
					22.0717865210637
				],
				[
					-87.21040845724394,
					22.610114262795037
				],
				[
					-87.74873619897528,
					23.148462540413334
				],
				[
					-89.36376049594332,
					24.763466301494304
				],
				[
					-90.440415979406,
					25.840142320843995
				],
				[
					-92.05544027637393,
					27.455146081925022
				],
				[
					-92.59376801810527,
					27.99347382365636
				],
				[
					-93.1320957598366,
					28.531822101274656
				],
				[
					-94.2087923150732,
					30.146825862355627
				],
				[
					-95.8237755402672,
					31.223501881705374
				],
				[
					-95.8237755402672,
					31.76182962343671
				],
				[
					-96.36214435377258,
					32.838505642786345
				],
				[
					-96.90047209550391,
					33.91518166213598
				],
				[
					-97.97712757896659,
					34.99183714559865
				],
				[
					-98.51545532069792,
					34.99183714559865
				],
				[
					-98.51545532069792,
					36.6068614425667
				],
				[
					-99.59215187593463,
					36.6068614425667
				],
				[
					-100.13047961766597,
					37.68351692602937
				],
				[
					-100.13047961766597,
					38.760192945379
				],
				[
					-101.20713510112864,
					39.2985412229973
				],
				[
					-101.7455039146339,
					40.375196706459974
				],
				[
					-102.28383165636524,
					40.91354498407833
				],
				[
					-102.28383165636524,
					41.99022100342802
				],
				[
					-103.36048713982791,
					42.528548745159355
				],
				[
					-103.89881488155925,
					44.143552506240326
				],
				[
					-104.97551143679595,
					44.143552506240326
				],
				[
					-104.97551143679595,
					45.758556267321296
				],
				[
					-105.51383917852729,
					46.29690454493965
				],
				[
					-105.51383917852729,
					47.37358056428934
				],
				[
					-106.59049466198985,
					47.91190830602068
				],
				[
					-106.59049466198985,
					48.450236047752014
				],
				[
					-107.12886347549534,
					48.450236047752014
				],
				[
					-107.12886347549534,
					49.52691206710165
				],
				[
					-107.12886347549534,
					50.065260344719945
				],
				[
					-107.12886347549534,
					51.14191582818262
				],
				[
					-107.12886347549534,
					51.68026410580097
				],
				[
					-107.12886347549534,
					52.75694012515066
				],
				[
					-107.66719121722667,
					53.295267866882
				],
				[
					-107.66719121722667,
					53.83359560861334
				],
				[
					-107.66719121722667,
					54.91027162796297
				],
				[
					-108.74384670068935,
					55.448619905581324
				],
				[
					-108.74384670068935,
					56.525275389044
				],
				[
					-108.20551895895801,
					56.525275389044
				],
				[
					-108.20551895895801,
					57.06362366666235
				],
				[
					-108.20551895895801,
					57.60195140839369
				],
				[
					-108.20551895895801,
					58.67862742774332
				],
				[
					-108.20551895895801,
					59.21695516947466
				],
				[
					-107.66719121722667,
					59.21695516947466
				],
				[
					-107.66719121722667,
					60.29363118882429
				],
				[
					-107.66719121722667,
					60.83197946644265
				],
				[
					-107.66719121722667,
					60.83197946644265
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 179,
			"versionNonce": 2125938909,
			"isDeleted": false,
			"id": "mE8WHe-TG33DW3NWINMp2",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 657.7036538868422,
			"y": 379.2992753955675,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 13.996726643884585,
			"height": 6.998363321942293,
			"seed": 1289047592,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.0766554834626731,
					0
				],
				[
					1.6149832251940097,
					0
				],
				[
					1.6149832251940097,
					0.5383277417313366
				],
				[
					1.6149832251940097,
					1.6150037610809704
				],
				[
					2.6916797804306043,
					2.153331502812307
				],
				[
					2.6916797804306043,
					3.230007522161941
				],
				[
					3.230007522161941,
					3.230007522161941
				],
				[
					3.230007522161941,
					3.768355799780295
				],
				[
					3.230007522161941,
					4.845011283242968
				],
				[
					3.7683352638932774,
					4.845011283242968
				],
				[
					3.7683352638932774,
					5.383359560861322
				],
				[
					3.7683352638932774,
					5.921687302592659
				],
				[
					4.844990747355951,
					5.921687302592659
				],
				[
					4.844990747355951,
					6.998363321942293
				],
				[
					5.383359560861322,
					6.998363321942293
				],
				[
					6.460015044323882,
					6.998363321942293
				],
				[
					6.998342786055218,
					6.998363321942293
				],
				[
					7.536670527786555,
					6.998363321942293
				],
				[
					8.613367083023377,
					6.998363321942293
				],
				[
					9.1516948247546,
					6.998363321942293
				],
				[
					10.228350308217273,
					6.460035580210956
				],
				[
					10.228350308217273,
					5.921687302592659
				],
				[
					10.766719121722645,
					5.921687302592659
				],
				[
					11.843374605185318,
					5.383359560861322
				],
				[
					11.843374605185318,
					4.306683541511632
				],
				[
					12.381702346916654,
					4.306683541511632
				],
				[
					12.92003008864799,
					3.768355799780295
				],
				[
					13.996726643884585,
					2.6916797804306043
				],
				[
					13.996726643884585,
					2.153331502812307
				],
				[
					13.996726643884585,
					2.153331502812307
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 220,
			"versionNonce": 1543473011,
			"isDeleted": false,
			"id": "VfGBjB9-WWgp04yjgiQU9",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 651.7819255124755,
			"y": 397.6026855809638,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 37.68351692602937,
			"height": 39.2985412229973,
			"seed": 591686488,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.6149832251940097,
					0
				],
				[
					-2.1533109669253463,
					0
				],
				[
					-3.230007522161941,
					0.5383482776183541
				],
				[
					-4.844990747355951,
					0.5383482776183541
				],
				[
					-5.383359560861322,
					0.5383482776183541
				],
				[
					-6.998342786055332,
					0.5383482776183541
				],
				[
					-7.536670527786669,
					0.5383482776183541
				],
				[
					-8.613367083023377,
					1.6150242969680448
				],
				[
					-9.151694824754713,
					1.6150242969680448
				],
				[
					-10.228350308217387,
					2.1533520386993814
				],
				[
					-10.766719121722645,
					2.1533520386993814
				],
				[
					-11.305046863453981,
					2.1533520386993814
				],
				[
					-12.92003008864799,
					2.1533520386993814
				],
				[
					-13.996726643884585,
					3.2300280580490153
				],
				[
					-15.611709869078595,
					3.768355799780352
				],
				[
					-16.150078682583967,
					3.768355799780352
				],
				[
					-16.688406424315303,
					3.768355799780352
				],
				[
					-17.765061907777977,
					4.845031819129986
				],
				[
					-18.303389649509313,
					4.845031819129986
				],
				[
					-20.456741688208695,
					5.383359560861322
				],
				[
					-21.53343824344529,
					5.921707838479676
				],
				[
					-22.071765985176626,
					6.998383857829367
				],
				[
					-23.1484214686393,
					6.998383857829367
				],
				[
					-23.686749210370635,
					7.536711599560704
				],
				[
					-24.76344576560723,
					7.536711599560704
				],
				[
					-25.301773507338567,
					7.536711599560704
				],
				[
					-25.301773507338567,
					8.613387618910338
				],
				[
					-25.840101249069903,
					8.613387618910338
				],
				[
					-26.916797804306725,
					8.613387618910338
				],
				[
					-26.916797804306725,
					9.151715360641674
				],
				[
					-27.45512554603806,
					9.151715360641674
				],
				[
					-27.45512554603806,
					9.690063638259971
				],
				[
					-28.53178102950062,
					9.690063638259971
				],
				[
					-28.53178102950062,
					10.766719121722645
				],
				[
					-29.070108771231958,
					10.766719121722645
				],
				[
					-29.070108771231958,
					11.305067399340999
				],
				[
					-30.146805326468666,
					11.305067399340999
				],
				[
					-30.146805326468666,
					12.38174341869069
				],
				[
					-30.685133068200003,
					12.920071160422026
				],
				[
					-30.685133068200003,
					13.99674717977166
				],
				[
					-31.22346080993134,
					14.535074921502996
				],
				[
					-31.22346080993134,
					15.073423199121294
				],
				[
					-32.300157365167934,
					16.150078682583967
				],
				[
					-32.300157365167934,
					16.68842696020232
				],
				[
					-32.83848510689927,
					17.76510297955201
				],
				[
					-32.83848510689927,
					18.30343072128335
				],
				[
					-33.91514059036194,
					19.380106740632982
				],
				[
					-33.91514059036194,
					19.91843448236432
				],
				[
					-34.45346833209328,
					20.456782759982616
				],
				[
					-34.45346833209328,
					21.53343824344529
				],
				[
					-34.99183714559865,
					22.071786521063643
				],
				[
					-34.99183714559865,
					23.148462540413334
				],
				[
					-36.068492629061325,
					23.68679028214467
				],
				[
					-36.068492629061325,
					24.763466301494304
				],
				[
					-36.068492629061325,
					25.30179404322564
				],
				[
					-36.60682037079266,
					25.840142320843995
				],
				[
					-36.60682037079266,
					26.91679780430667
				],
				[
					-36.60682037079266,
					27.455146081925022
				],
				[
					-36.60682037079266,
					28.531822101274656
				],
				[
					-36.60682037079266,
					29.070149843005993
				],
				[
					-36.60682037079266,
					29.60847758473733
				],
				[
					-36.60682037079266,
					30.685153604086963
				],
				[
					-36.60682037079266,
					31.223501881705317
				],
				[
					-36.60682037079266,
					32.30015736516799
				],
				[
					-36.60682037079266,
					32.838505642786345
				],
				[
					-36.60682037079266,
					33.91518166213598
				],
				[
					-36.60682037079266,
					34.453509403867315
				],
				[
					-36.60682037079266,
					34.99183714559865
				],
				[
					-36.60682037079266,
					36.068513164948286
				],
				[
					-36.60682037079266,
					36.60686144256664
				],
				[
					-36.60682037079266,
					37.68351692602931
				],
				[
					-37.68351692602937,
					38.22186520364767
				],
				[
					-37.68351692602937,
					39.2985412229973
				],
				[
					-37.68351692602937,
					39.2985412229973
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 170,
			"versionNonce": 188030269,
			"isDeleted": false,
			"id": "xx5rpdmQQwpLrFqUWiOpU",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 611.4067288060155,
			"y": 435.82455078461146,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 9.151735896528635,
			"height": 5.921687302592659,
			"seed": 848979800,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.538368813505258,
					0
				],
				[
					1.6150242969679311,
					1.0766760193496339
				],
				[
					1.6150242969679311,
					1.6150037610809704
				],
				[
					1.6150242969679311,
					2.153331502812307
				],
				[
					2.1533520386992677,
					3.230007522161941
				],
				[
					2.1533520386992677,
					3.768355799780295
				],
				[
					2.1533520386992677,
					4.845011283242968
				],
				[
					3.230048593935976,
					5.383359560861322
				],
				[
					3.230048593935976,
					5.921687302592659
				],
				[
					3.7683763356673126,
					5.921687302592659
				],
				[
					4.845031819129986,
					5.921687302592659
				],
				[
					5.383359560861322,
					5.921687302592659
				],
				[
					5.383359560861322,
					5.383359560861322
				],
				[
					5.921728374366694,
					5.383359560861322
				],
				[
					5.921728374366694,
					4.306683541511632
				],
				[
					6.998383857829367,
					4.306683541511632
				],
				[
					6.998383857829367,
					3.768355799780295
				],
				[
					7.536711599560704,
					2.6916797804306043
				],
				[
					7.536711599560704,
					2.153331502812307
				],
				[
					8.613408154797298,
					2.153331502812307
				],
				[
					8.613408154797298,
					1.6150037610809704
				],
				[
					9.151735896528635,
					1.6150037610809704
				],
				[
					9.151735896528635,
					0.5383277417313366
				],
				[
					9.151735896528635,
					0.5383277417313366
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 204,
			"versionNonce": 1143218451,
			"isDeleted": false,
			"id": "N7gsoxl4JfObnTzoemrPK",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 600.6400096842929,
			"y": 457.8963167697881,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 17.765061907777977,
			"height": 39.2985412229973,
			"seed": 23587160,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.0766760193496339
				],
				[
					0,
					1.6150037610809704
				],
				[
					0,
					2.691679780430718
				],
				[
					-1.0766554834626731,
					2.691679780430718
				],
				[
					-1.0766554834626731,
					3.2300280580490153
				],
				[
					-1.6149832251940097,
					4.845031819129986
				],
				[
					-2.6916797804306043,
					5.383359560861322
				],
				[
					-3.230007522161941,
					6.460035580210956
				],
				[
					-3.230007522161941,
					6.998363321942293
				],
				[
					-3.7683352638932774,
					8.07503934129204
				],
				[
					-4.844990747355951,
					8.613387618910338
				],
				[
					-4.844990747355951,
					9.151715360641674
				],
				[
					-5.383359560861322,
					10.228391379991308
				],
				[
					-6.460015044323995,
					10.766719121722645
				],
				[
					-6.460015044323995,
					11.843395141072278
				],
				[
					-6.998342786055332,
					11.843395141072278
				],
				[
					-6.998342786055332,
					12.381722882803615
				],
				[
					-8.07503934129204,
					13.458398902153363
				],
				[
					-8.613367083023377,
					13.458398902153363
				],
				[
					-8.613367083023377,
					13.99674717977166
				],
				[
					-9.151694824754713,
					14.535074921502996
				],
				[
					-10.228350308217387,
					15.61175094085263
				],
				[
					-10.228350308217387,
					16.150078682583967
				],
				[
					-10.766719121722645,
					16.150078682583967
				],
				[
					-10.766719121722645,
					17.2267547019336
				],
				[
					-11.843374605185318,
					17.2267547019336
				],
				[
					-11.843374605185318,
					17.765082443664937
				],
				[
					-11.843374605185318,
					18.30343072128335
				],
				[
					-12.381702346916654,
					18.30343072128335
				],
				[
					-12.381702346916654,
					19.380106740632982
				],
				[
					-12.381702346916654,
					19.91843448236432
				],
				[
					-13.458398902153249,
					20.995110501713953
				],
				[
					-13.458398902153249,
					21.53343824344529
				],
				[
					-13.458398902153249,
					22.610114262795037
				],
				[
					-13.996726643884585,
					23.148442004526373
				],
				[
					-13.996726643884585,
					23.68679028214467
				],
				[
					-13.996726643884585,
					24.763466301494304
				],
				[
					-13.996726643884585,
					25.30179404322564
				],
				[
					-13.996726643884585,
					26.378470062575275
				],
				[
					-14.535054385615922,
					26.91679780430661
				],
				[
					-14.535054385615922,
					27.99347382365636
				],
				[
					-14.535054385615922,
					28.531801565387696
				],
				[
					-14.535054385615922,
					29.070149843005993
				],
				[
					-15.611709869078595,
					30.146805326468666
				],
				[
					-15.611709869078595,
					30.685174139973924
				],
				[
					-15.611709869078595,
					31.761829623436597
				],
				[
					-15.611709869078595,
					32.300157365167934
				],
				[
					-15.611709869078595,
					33.37685392040464
				],
				[
					-16.150078682583967,
					33.91518166213598
				],
				[
					-16.150078682583967,
					34.453509403867315
				],
				[
					-16.150078682583967,
					35.53016488732999
				],
				[
					-17.22673416604664,
					35.53016488732999
				],
				[
					-17.22673416604664,
					36.06853370083536
				],
				[
					-17.22673416604664,
					37.14518918429792
				],
				[
					-17.22673416604664,
					37.683516926029256
				],
				[
					-17.22673416604664,
					38.22184466776059
				],
				[
					-17.765061907777977,
					39.2985412229973
				],
				[
					-17.765061907777977,
					39.2985412229973
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 168,
			"versionNonce": 410545565,
			"isDeleted": false,
			"id": "tU6J_u_87LzahItrBmeJq",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 576.9532604739222,
			"y": 492.3498261736554,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 9.69002256648605,
			"height": 5.383359560861322,
			"seed": 515725656,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.5383277417313366,
					0
				],
				[
					1.6149832251940097,
					0
				],
				[
					2.1533109669253463,
					0
				],
				[
					2.1533109669253463,
					1.0766554834626731
				],
				[
					3.230007522161941,
					1.0766554834626731
				],
				[
					3.230007522161941,
					1.6150242969680448
				],
				[
					3.7683352638932774,
					2.6916797804306043
				],
				[
					3.7683352638932774,
					3.230007522161941
				],
				[
					4.306663005624614,
					3.7683352638932774
				],
				[
					4.306663005624614,
					4.845031819129986
				],
				[
					4.306663005624614,
					5.383359560861322
				],
				[
					5.383359560861322,
					5.383359560861322
				],
				[
					5.921687302592659,
					5.383359560861322
				],
				[
					6.998342786055332,
					5.383359560861322
				],
				[
					7.536670527786669,
					5.383359560861322
				],
				[
					7.536670527786669,
					4.306704077398649
				],
				[
					8.613367083023377,
					4.306704077398649
				],
				[
					8.613367083023377,
					3.7683352638932774
				],
				[
					9.151694824754713,
					3.7683352638932774
				],
				[
					9.151694824754713,
					3.230007522161941
				],
				[
					9.69002256648605,
					3.230007522161941
				],
				[
					9.69002256648605,
					2.1533520386992677
				],
				[
					9.69002256648605,
					2.1533520386992677
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 193,
			"versionNonce": 465864371,
			"isDeleted": false,
			"id": "J6Xycuz5kyqaqpxeBQlTT",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 575.3382361769542,
			"y": 515.4982887140687,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 17.765102979551898,
			"height": 27.455125546037948,
			"seed": 918480472,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.0766554834625595,
					0
				],
				[
					-1.0766554834625595,
					0.5383277417313366
				],
				[
					-1.6150242969680448,
					0.5383277417313366
				],
				[
					-2.691679780430718,
					1.6149832251940097
				],
				[
					-2.691679780430718,
					2.1533109669253463
				],
				[
					-3.2300075221620546,
					2.1533109669253463
				],
				[
					-3.768335263893391,
					3.230007522161941
				],
				[
					-3.768335263893391,
					3.7683352638932774
				],
				[
					-3.768335263893391,
					4.844990747355951
				],
				[
					-4.845031819129986,
					4.844990747355951
				],
				[
					-4.845031819129986,
					5.383359560861322
				],
				[
					-5.383359560861322,
					5.383359560861322
				],
				[
					-6.460015044323995,
					5.921687302592659
				],
				[
					-6.998383857829253,
					6.998342786055332
				],
				[
					-8.075039341291927,
					7.536670527786669
				],
				[
					-8.075039341291927,
					8.613367083023263
				],
				[
					-8.613367083023263,
					8.613367083023263
				],
				[
					-8.613367083023263,
					9.1516948247546
				],
				[
					-9.1516948247546,
					10.228350308217273
				],
				[
					-10.228391379991308,
					10.766719121722645
				],
				[
					-10.766719121722645,
					10.766719121722645
				],
				[
					-10.766719121722645,
					11.305046863453981
				],
				[
					-11.843374605185318,
					11.305046863453981
				],
				[
					-11.843374605185318,
					12.381702346916654
				],
				[
					-12.38174341869069,
					12.381702346916654
				],
				[
					-12.38174341869069,
					12.92003008864799
				],
				[
					-12.920071160422026,
					13.996726643884585
				],
				[
					-12.920071160422026,
					14.535054385615922
				],
				[
					-13.9967266438847,
					14.535054385615922
				],
				[
					-14.535054385616036,
					15.073382127347259
				],
				[
					-15.61175094085263,
					16.150078682583967
				],
				[
					-15.61175094085263,
					16.688406424315303
				],
				[
					-15.61175094085263,
					17.765061907777977
				],
				[
					-16.150078682583967,
					18.303389649509313
				],
				[
					-16.150078682583967,
					19.380086204745908
				],
				[
					-17.22673416604664,
					19.918413946477244
				],
				[
					-17.22673416604664,
					20.45674168820858
				],
				[
					-17.22673416604664,
					21.53343824344529
				],
				[
					-17.22673416604664,
					22.071765985176626
				],
				[
					-17.22673416604664,
					23.1484214686393
				],
				[
					-17.22673416604664,
					23.686749210370635
				],
				[
					-17.22673416604664,
					24.76344576560723
				],
				[
					-17.22673416604664,
					25.301773507338567
				],
				[
					-17.765102979551898,
					25.301773507338567
				],
				[
					-17.765102979551898,
					25.840101249069903
				],
				[
					-17.765102979551898,
					26.91679780430661
				],
				[
					-17.765102979551898,
					27.455125546037948
				],
				[
					-17.765102979551898,
					27.455125546037948
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 167,
			"versionNonce": 1437774333,
			"isDeleted": false,
			"id": "qNPyZl4ySGoOmZEqSTYHZ",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 552.7281424500462,
			"y": 538.1083824409767,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 11.843374605185318,
			"height": 6.460015044323995,
			"seed": 154794280,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.0766554834626731,
					1.0766554834626731
				],
				[
					1.0766554834626731,
					1.6150242969680448
				],
				[
					1.6149832251940097,
					1.6150242969680448
				],
				[
					1.6149832251940097,
					2.6916797804306043
				],
				[
					2.691679780430718,
					3.230007522161941
				],
				[
					2.691679780430718,
					3.7683352638932774
				],
				[
					3.2300075221620546,
					3.7683352638932774
				],
				[
					3.2300075221620546,
					4.845031819129986
				],
				[
					4.306663005624728,
					4.845031819129986
				],
				[
					4.306663005624728,
					5.383359560861322
				],
				[
					4.844990747356064,
					6.460015044323995
				],
				[
					5.383359560861322,
					6.460015044323995
				],
				[
					6.460015044323995,
					5.921687302592659
				],
				[
					6.998342786055332,
					5.383359560861322
				],
				[
					8.075039341291927,
					4.306704077398649
				],
				[
					8.613367083023263,
					4.306704077398649
				],
				[
					8.613367083023263,
					3.7683352638932774
				],
				[
					9.1516948247546,
					3.7683352638932774
				],
				[
					10.228350308217273,
					3.230007522161941
				],
				[
					10.228350308217273,
					2.1533520386992677
				],
				[
					10.766719121722645,
					2.1533520386992677
				],
				[
					10.766719121722645,
					1.6150242969680448
				],
				[
					11.843374605185318,
					1.6150242969680448
				],
				[
					11.843374605185318,
					1.6150242969680448
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 228,
			"versionNonce": 428292179,
			"isDeleted": false,
			"id": "DxOH6DDSI7kzazDey4JlK",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 623.0955433454808,
			"y": 507.0210856773708,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 20.46601912561937,
			"height": 36.46672214849764,
			"seed": 1817371480,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.37210376070811435,
					0
				],
				[
					0.37210376070811435,
					0.744221716264974
				],
				[
					1.1163396718216063,
					0.744221716264974
				],
				[
					1.488443432529948,
					0.744221716264974
				],
				[
					1.8605471932380624,
					1.1163254769731452
				],
				[
					2.6047831043515544,
					1.1163254769731452
				],
				[
					2.9768868650597824,
					1.488443432529948
				],
				[
					3.721094386476125,
					1.488443432529948
				],
				[
					4.0931981471844665,
					2.2326509539462904
				],
				[
					4.8374340582979585,
					2.2326509539462904
				],
				[
					4.8374340582979585,
					2.6047689095030933
				],
				[
					5.209537819006073,
					2.6047689095030933
				],
				[
					5.5816415797144145,
					3.3489906257680673
				],
				[
					6.3258774908279065,
					3.3489906257680673
				],
				[
					6.697981251536021,
					3.7210943864762385
				],
				[
					7.442188772952477,
					3.7210943864762385
				],
				[
					7.442188772952477,
					4.4653161027412125
				],
				[
					7.814292533660591,
					4.4653161027412125
				],
				[
					7.814292533660591,
					4.8374198634494405
				],
				[
					8.558528444774197,
					4.8374198634494405
				],
				[
					8.558528444774197,
					5.2095378190061865
				],
				[
					8.930632205482425,
					5.2095378190061865
				],
				[
					9.30273596619054,
					5.953745340422529
				],
				[
					9.30273596619054,
					6.325863295979389
				],
				[
					10.046971877304145,
					6.325863295979389
				],
				[
					10.419075638012373,
					7.070085012244363
				],
				[
					10.419075638012373,
					7.442188772952477
				],
				[
					11.163283159428715,
					7.442188772952477
				],
				[
					11.163283159428715,
					8.186410489217451
				],
				[
					11.535386920136943,
					8.186410489217451
				],
				[
					11.535386920136943,
					8.558514249925679
				],
				[
					11.907519070542321,
					8.930632205482425
				],
				[
					12.651726591958663,
					9.674839726898881
				],
				[
					12.651726591958663,
					10.046957682455627
				],
				[
					12.651726591958663,
					10.791179398720601
				],
				[
					13.023830352666891,
					10.791179398720601
				],
				[
					13.023830352666891,
					11.163283159428829
				],
				[
					13.768066263780383,
					11.535386920136943
				],
				[
					14.140170024488611,
					12.279608636401917
				],
				[
					14.140170024488611,
					12.651726591958777
				],
				[
					14.884377545904954,
					13.39593411337512
				],
				[
					14.884377545904954,
					13.768052068931866
				],
				[
					15.256481306613182,
					14.51227378519684
				],
				[
					15.256481306613182,
					14.884377545905068
				],
				[
					15.62861345701856,
					15.256481306613296
				],
				[
					15.62861345701856,
					16.00070302287827
				],
				[
					15.62861345701856,
					16.372820978435016
				],
				[
					15.62861345701856,
					17.117028499851358
				],
				[
					16.372820978434902,
					18.23336817167319
				],
				[
					16.74492473914313,
					18.23336817167319
				],
				[
					16.74492473914313,
					18.605471932381306
				],
				[
					16.74492473914313,
					18.977575693089534
				],
				[
					17.489160650256736,
					19.721797409354508
				],
				[
					17.489160650256736,
					20.093915364911254
				],
				[
					17.86126441096485,
					20.83812288632771
				],
				[
					17.86126441096485,
					21.210240841884456
				],
				[
					17.86126441096485,
					21.95446255814943
				],
				[
					17.86126441096485,
					22.326566318857658
				],
				[
					18.605471932381306,
					22.698670079565773
				],
				[
					18.605471932381306,
					23.442891795830747
				],
				[
					18.605471932381306,
					23.815009751387606
				],
				[
					18.605471932381306,
					24.55921727280395
				],
				[
					18.97757569308942,
					24.931335228360695
				],
				[
					18.97757569308942,
					25.303438989068923
				],
				[
					19.349707843494798,
					26.047660705333897
				],
				[
					19.349707843494798,
					26.419764466042125
				],
				[
					19.349707843494798,
					27.1639861823071
				],
				[
					20.093915364911254,
					27.536104137863845
				],
				[
					20.093915364911254,
					28.280311659280187
				],
				[
					20.093915364911254,
					28.652429614836933
				],
				[
					20.093915364911254,
					29.02453337554516
				],
				[
					20.093915364911254,
					29.768755091810135
				],
				[
					20.46601912561937,
					29.768755091810135
				],
				[
					20.46601912561937,
					30.140858852518363
				],
				[
					20.46601912561937,
					30.885080568783337
				],
				[
					20.46601912561937,
					31.257198524340083
				],
				[
					20.46601912561937,
					32.001406045756426
				],
				[
					20.46601912561937,
					32.37352400131317
				],
				[
					20.46601912561937,
					32.7456277620214
				],
				[
					20.46601912561937,
					33.489849478286374
				],
				[
					20.46601912561937,
					33.8619532389946
				],
				[
					20.46601912561937,
					34.606174955259576
				],
				[
					20.46601912561937,
					34.97829291081632
				],
				[
					20.46601912561937,
					35.35039667152455
				],
				[
					20.46601912561937,
					36.094618387789524
				],
				[
					20.46601912561937,
					36.46672214849764
				],
				[
					20.46601912561937,
					36.46672214849764
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 173,
			"versionNonce": 266693213,
			"isDeleted": false,
			"id": "fEd6NI4mTxVWIziecUymW",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 639.4683643239157,
			"y": 539.394609678684,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 10.046943487607109,
			"height": 6.325849101130871,
			"seed": 1471574104,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.37210376070822804,
					0
				],
				[
					1.1163396718218337,
					0.37210376070822804
				],
				[
					1.1163396718218337,
					1.116325476973202
				],
				[
					1.1163396718218337,
					1.48842923768143
				],
				[
					1.1163396718218337,
					2.232650953946404
				],
				[
					1.488443432529948,
					2.232650953946404
				],
				[
					1.488443432529948,
					2.60476890950315
				],
				[
					1.488443432529948,
					2.976872670211378
				],
				[
					1.488443432529948,
					3.721094386476352
				],
				[
					2.232650953946404,
					4.0931981471844665
				],
				[
					2.232650953946404,
					4.8374198634494405
				],
				[
					2.6047547146545185,
					4.8374198634494405
				],
				[
					2.6047547146545185,
					5.209523624157669
				],
				[
					2.6047547146545185,
					5.953745340422643
				],
				[
					2.976886865059896,
					5.953745340422643
				],
				[
					2.976886865059896,
					6.325849101130871
				],
				[
					3.721094386476352,
					6.325849101130871
				],
				[
					4.0931981471844665,
					6.325849101130871
				],
				[
					4.837434058298072,
					6.325849101130871
				],
				[
					5.2095378190063,
					6.325849101130871
				],
				[
					5.953745340422643,
					6.325849101130871
				],
				[
					5.953745340422643,
					5.5816415797144145
				],
				[
					6.325849101130871,
					5.5816415797144145
				],
				[
					6.697981251536248,
					5.209523624157669
				],
				[
					7.442188772952591,
					5.209523624157669
				],
				[
					7.814292533660819,
					4.465316102741326
				],
				[
					8.55852844477431,
					4.465316102741326
				],
				[
					8.930632205482539,
					4.0931981471844665
				],
				[
					9.302735966190767,
					4.0931981471844665
				],
				[
					9.302735966190767,
					3.3489764309194925
				],
				[
					10.046943487607109,
					3.3489764309194925
				],
				[
					10.046943487607109,
					3.3489764309194925
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 210,
			"versionNonce": 1531098611,
			"isDeleted": false,
			"id": "aIZI0UjBZ8jJar0Z9ljAu",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 585.3271457459686,
			"y": 551.6312101969116,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 10.766987988437108,
			"height": 13.240493929624222,
			"seed": 2014838824,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.2909954750734869,
					0
				],
				[
					0.43649321261011664,
					0
				],
				[
					0.5819909501468601,
					0
				],
				[
					0.8729975259860794,
					0
				],
				[
					1.0184952635227091,
					0
				],
				[
					1.309490738596196,
					0
				],
				[
					1.4549995768986719,
					0
				],
				[
					1.745995051972045,
					-0.2909954750733732
				],
				[
					1.8914927895087885,
					-0.2909954750733732
				],
				[
					2.0369905270454183,
					-0.2909954750733732
				],
				[
					2.3279971028846376,
					-0.43649321261011664
				],
				[
					2.473494840421381,
					-0.43649321261011664
				],
				[
					2.473494840421381,
					-0.7274997884493359
				],
				[
					2.764490315494754,
					-0.7274997884493359
				],
				[
					2.90999915379723,
					-0.8729975259860794
				],
				[
					3.200994628870717,
					-1.0184952635227091
				],
				[
					3.49199010394409,
					-1.3095018393619284
				],
				[
					3.7829966797833094,
					-1.4549995768986719
				],
				[
					3.928494417319939,
					-1.745995051972045
				],
				[
					4.219489892393426,
					-1.8914927895087885
				],
				[
					4.510496468232645,
					-2.3279971028846376
				],
				[
					4.510496468232645,
					-2.473494840421381
				],
				[
					4.946989680842648,
					-2.7645014162606003
				],
				[
					5.237996256681868,
					-3.2009946288706033
				],
				[
					5.383493994218611,
					-3.3464923664073467
				],
				[
					5.674489469291984,
					-3.4920012047098226
				],
				[
					5.819998307594574,
					-3.7829966797831958
				],
				[
					5.965496045131204,
					-3.928494417319939
				],
				[
					6.256491520204577,
					-4.2195009931591585
				],
				[
					6.40198925774132,
					-4.2195009931591585
				],
				[
					6.40198925774132,
					-4.364998730695902
				],
				[
					6.6929958335805395,
					-4.364998730695902
				],
				[
					6.6929958335805395,
					-4.655994205769275
				],
				[
					6.838493571117283,
					-4.801491943305905
				],
				[
					7.129489046190656,
					-4.947000781608494
				],
				[
					7.274997884493132,
					-5.237996256681868
				],
				[
					7.274997884493132,
					-5.383499544601477
				],
				[
					7.4204956220298754,
					-5.6744950196748505
				],
				[
					7.4204956220298754,
					-5.81999830759446
				],
				[
					7.711491097103249,
					-6.110999333050813
				],
				[
					7.856988834639878,
					-6.256497070587443
				],
				[
					8.147995410479098,
					-6.6929958335805395
				],
				[
					8.147995410479098,
					-6.838499121500149
				],
				[
					8.293493148015841,
					-7.274997884493132
				],
				[
					8.584488623089214,
					-7.711496647486115
				],
				[
					8.72999746139169,
					-7.856994385022858
				],
				[
					8.72999746139169,
					-8.147995410479098
				],
				[
					8.875495198928434,
					-8.293498698398707
				],
				[
					8.875495198928434,
					-8.58449417347208
				],
				[
					9.166490674001807,
					-8.875495198928434
				],
				[
					9.31198841153855,
					-9.166496224384673
				],
				[
					9.31198841153855,
					-9.311993961921416
				],
				[
					9.31198841153855,
					-9.60299498737777
				],
				[
					9.31198841153855,
					-9.74849827529738
				],
				[
					9.60299498737777,
					-10.039493750370752
				],
				[
					9.7484927249144,
					-10.330494775826992
				],
				[
					9.893990462451143,
					-10.621495801283345
				],
				[
					9.893990462451143,
					-10.766993538819975
				],
				[
					10.184997038290362,
					-10.766993538819975
				],
				[
					10.184997038290362,
					-11.057994564276328
				],
				[
					10.184997038290362,
					-11.203497852195937
				],
				[
					10.330494775827106,
					-11.203497852195937
				],
				[
					10.330494775827106,
					-11.34899558973268
				],
				[
					10.330494775827106,
					-11.63999661518892
				],
				[
					10.330494775827106,
					-11.785494352725664
				],
				[
					10.330494775827106,
					-12.076495378181903
				],
				[
					10.330494775827106,
					-12.221993115718647
				],
				[
					10.621490250900479,
					-12.512994141175
				],
				[
					10.621490250900479,
					-12.65849742909461
				],
				[
					10.621490250900479,
					-12.803995166631239
				],
				[
					10.766987988437108,
					-13.094996192087592
				],
				[
					10.766987988437108,
					-13.240493929624222
				],
				[
					10.766987988437108,
					-13.240493929624222
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 195,
			"versionNonce": 2011305661,
			"isDeleted": false,
			"id": "v83YgnZ1iMG7nIPvA07r0",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 596.2119694249006,
			"y": 528.1837586604817,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 5.5176592657136325,
			"height": 6.95701084032919,
			"seed": 266348840,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.47978690865477347,
					0
				],
				[
					0.47978690865477347,
					-0.2398934543273299
				],
				[
					0.7196803629821034,
					-0.2398934543273299
				],
				[
					0.7196803629821034,
					-0.7196895143307529
				],
				[
					1.199485574334176,
					-0.9595829686581965
				],
				[
					1.4393790286615058,
					-0.9595829686581965
				],
				[
					1.4393790286615058,
					-1.199485574334176
				],
				[
					1.9191659373162793,
					-1.6792724829889494
				],
				[
					2.159059391643723,
					-1.6792724829889494
				],
				[
					2.159059391643723,
					-1.4393790286616195
				],
				[
					2.398971148668352,
					-1.199485574334176
				],
				[
					2.398971148668352,
					-0.9595829686581965
				],
				[
					2.398971148668352,
					-0.47978690865477347
				],
				[
					2.398971148668352,
					-0.2398934543273299
				],
				[
					2.398971148668352,
					0.23990260567609312
				],
				[
					2.398971148668352,
					0.479796060003423
				],
				[
					2.398971148668352,
					0.7196986656794024
				],
				[
					2.398971148668352,
					1.199485574334176
				],
				[
					2.398971148668352,
					1.919184240013692
				],
				[
					2.398971148668352,
					2.159077694341022
				],
				[
					2.398971148668352,
					2.638873754344445
				],
				[
					2.398971148668352,
					2.878767208671775
				],
				[
					2.398971148668352,
					3.118669814347868
				],
				[
					2.398971148668352,
					3.5984567230026414
				],
				[
					2.398971148668352,
					3.838359328678621
				],
				[
					2.8787580573231253,
					4.318155388682044
				],
				[
					2.8787580573231253,
					4.558048843009487
				],
				[
					2.6388646029957954,
					4.558048843009487
				],
				[
					2.398971148668352,
					4.558048843009487
				],
				[
					2.159059391643723,
					4.558048843009487
				],
				[
					1.6792724829889494,
					4.558048843009487
				],
				[
					1.4393790286615058,
					4.558048843009487
				],
				[
					0.9595738173094333,
					4.558048843009487
				],
				[
					0.7196803629821034,
					4.558048843009487
				],
				[
					0.2398934543273299,
					4.558048843009487
				],
				[
					0,
					4.558048843009487
				],
				[
					0,
					4.078252783006064
				],
				[
					-0.23991175702474266,
					4.078252783006064
				],
				[
					-0.23991175702474266,
					4.318155388682044
				],
				[
					0,
					4.318155388682044
				],
				[
					0.47978690865477347,
					4.318155388682044
				],
				[
					0.47978690865477347,
					4.558048843009487
				],
				[
					0.7196803629821034,
					4.558048843009487
				],
				[
					1.199485574334176,
					4.558048843009487
				],
				[
					1.4393790286615058,
					4.558048843009487
				],
				[
					1.9191659373162793,
					5.03784490301291
				],
				[
					2.159059391643723,
					5.03784490301291
				],
				[
					2.398971148668352,
					5.03784490301291
				],
				[
					2.398971148668352,
					5.27773835734024
				],
				[
					2.8787580573231253,
					5.27773835734024
				],
				[
					3.118651511650569,
					5.27773835734024
				],
				[
					3.5984384203052286,
					5.27773835734024
				],
				[
					3.8383501773299713,
					5.27773835734024
				],
				[
					4.078261934354714,
					5.27773835734024
				],
				[
					4.558048843009487,
					5.27773835734024
				],
				[
					4.7979239946394046,
					5.27773835734024
				],
				[
					5.27774750868889,
					5.27773835734024
				],
				[
					5.27774750868889,
					5.27773835734024
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 161,
			"versionNonce": 2147319699,
			"isDeleted": false,
			"id": "CHWOy0ibFqtHTW-lihdJN",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 598.610940573569,
			"y": 523.3858163631448,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 1.4393790286616195,
			"height": 7.196913446005283,
			"seed": 1613675816,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.23989345432744358
				],
				[
					0,
					-0.7196895143308666
				],
				[
					0,
					-0.9595829686581965
				],
				[
					0,
					-1.199485574334176
				],
				[
					0.47978690865477347,
					-1.199485574334176
				],
				[
					0.47978690865477347,
					-1.6792724829889494
				],
				[
					0.47978690865477347,
					-1.9191750886650425
				],
				[
					0.719680362982217,
					-2.3989711486684655
				],
				[
					0.719680362982217,
					-2.6388646029957954
				],
				[
					0.719680362982217,
					-2.878758057323239
				],
				[
					0.719680362982217,
					-3.3585541173265483
				],
				[
					0.719680362982217,
					-3.5984567230026414
				],
				[
					0.719680362982217,
					-4.078243631657415
				],
				[
					0.719680362982217,
					-4.318146237333394
				],
				[
					0.719680362982217,
					-4.797942297336817
				],
				[
					0.719680362982217,
					-5.037835751664261
				],
				[
					1.1994672716368768,
					-5.277729205991591
				],
				[
					1.1994672716368768,
					-5.757525265995014
				],
				[
					1.1994672716368768,
					-5.997427871671107
				],
				[
					1.4393790286616195,
					-6.477214780325767
				],
				[
					1.4393790286616195,
					-6.71711738600186
				],
				[
					1.4393790286616195,
					-7.196913446005283
				],
				[
					1.4393790286616195,
					-6.95701084032919
				],
				[
					1.4393790286616195,
					-6.95701084032919
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 176,
			"versionNonce": 675952413,
			"isDeleted": false,
			"id": "UO1k_YLH9Pr0EeVn3JZeY",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 598.8508340278964,
			"y": 514.9894173428054,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 6.71710823465321,
			"height": 3.5984567230026414,
			"seed": 943495976,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.23989345432744358,
					0
				],
				[
					-0.47980521135207255,
					0
				],
				[
					-0.959592120006846,
					0
				],
				[
					-1.1994855743342896,
					0
				],
				[
					-1.6792907856863621,
					0
				],
				[
					-1.919184240013692,
					0.479796060003423
				],
				[
					-2.3989711486684655,
					0.479796060003423
				],
				[
					-2.6388646029957954,
					0.479796060003423
				],
				[
					-2.6388646029957954,
					0.7196986656794024
				],
				[
					-2.878776360020538,
					0.7196986656794024
				],
				[
					-3.3585632686753115,
					0.7196986656794024
				],
				[
					-3.118669814347868,
					0.7196986656794024
				],
				[
					-2.878776360020538,
					0.7196986656794024
				],
				[
					-2.6388646029957954,
					0.7196986656794024
				],
				[
					-2.159077694341022,
					0.23990260567597943
				],
				[
					-1.919184240013692,
					0.23990260567597943
				],
				[
					-1.4393790286616195,
					0
				],
				[
					-1.1994855743342896,
					0
				],
				[
					-0.7196986656795161,
					-0.47978690865477347
				],
				[
					-0.47980521135207255,
					-0.7196895143308666
				],
				[
					-0.23989345432744358,
					-0.7196895143308666
				],
				[
					0.2398934543273299,
					-0.7196895143308666
				],
				[
					0.47978690865477347,
					-0.7196895143308666
				],
				[
					0.9595738173094333,
					-0.7196895143308666
				],
				[
					1.199485574334176,
					-0.7196895143308666
				],
				[
					1.199485574334176,
					-0.23989345432744358
				],
				[
					1.4393973313589186,
					-0.23989345432744358
				],
				[
					1.919184240013692,
					0
				],
				[
					1.919184240013692,
					0.479796060003423
				],
				[
					2.159059391643609,
					0.479796060003423
				],
				[
					2.6388829056930945,
					0.7196986656794024
				],
				[
					2.6388829056930945,
					0.959592120006846
				],
				[
					2.8787580573231253,
					1.439388180010269
				],
				[
					2.8787580573231253,
					1.679281634337599
				],
				[
					2.8787580573231253,
					2.159077694341022
				],
				[
					3.3585449659778988,
					2.159077694341022
				],
				[
					3.3585449659778988,
					2.398971148668352
				],
				[
					3.3585449659778988,
					2.878767208671775
				],
				[
					3.3585449659778988,
					2.878767208671775
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 165,
			"versionNonce": 32380211,
			"isDeleted": false,
			"id": "nVDTqNhZWdtehn-AQUI7z",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 620.4415743659122,
			"y": 549.294702938494,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 7.196913446005283,
			"height": 6.717108234653097,
			"seed": 811608152,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.4797869086546598,
					0
				],
				[
					-0.4797869086546598,
					-0.2398934543273299
				],
				[
					-0.7196986656795161,
					-0.2398934543273299
				],
				[
					-0.7196986656795161,
					-0.7196803629821034
				],
				[
					-1.199485574334176,
					-0.7196803629821034
				],
				[
					-1.199485574334176,
					-0.9595738173094333
				],
				[
					-1.4393973313589186,
					-0.9595738173094333
				],
				[
					-1.919184240013692,
					-1.4393790286616195
				],
				[
					-2.159059391643723,
					-1.4393790286616195
				],
				[
					-2.159059391643723,
					-1.6792724829889494
				],
				[
					-2.398971148668352,
					-1.6792724829889494
				],
				[
					-2.8787580573231253,
					-2.159059391643609
				],
				[
					-3.118669814347868,
					-2.398971148668352
				],
				[
					-3.5984567230026414,
					-2.398971148668352
				],
				[
					-3.838368480027384,
					-2.398971148668352
				],
				[
					-4.078243631657415,
					-2.6388646029957954
				],
				[
					-4.078243631657415,
					-3.118651511650455
				],
				[
					-4.558030540312075,
					-3.118651511650455
				],
				[
					-4.558030540312075,
					-3.3585449659778988
				],
				[
					-4.797942297336817,
					-3.3585449659778988
				],
				[
					-5.277729205991591,
					-3.3585449659778988
				],
				[
					-5.277729205991591,
					-3.8383501773299713
				],
				[
					-5.51764096301622,
					-3.8383501773299713
				],
				[
					-5.51764096301622,
					-4.078243631657301
				],
				[
					-5.997427871670993,
					-4.318137085984745
				],
				[
					-6.237339628695736,
					-4.797942297336817
				],
				[
					-6.237339628695736,
					-5.037835751664147
				],
				[
					-6.237339628695736,
					-5.517622660318921
				],
				[
					-6.477214780325767,
					-5.517622660318921
				],
				[
					-6.477214780325767,
					-5.757516114646251
				],
				[
					-6.95700168898054,
					-6.237321325998323
				],
				[
					-6.95700168898054,
					-6.477214780325767
				],
				[
					-7.196913446005283,
					-6.477214780325767
				],
				[
					-7.196913446005283,
					-6.717108234653097
				],
				[
					-7.196913446005283,
					-6.717108234653097
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 208,
			"versionNonce": 1804553085,
			"isDeleted": false,
			"id": "yNdQWDG7qcuuz_OfDAKGh",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 609.6462041969044,
			"y": 533.701399623498,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 7.4368252030300255,
			"height": 6.95701084032919,
			"seed": 1834267480,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.47978690865477347,
					0
				],
				[
					-0.47978690865477347,
					0.2398934543273299
				],
				[
					-0.7196986656795161,
					0.2398934543273299
				],
				[
					-0.7196986656795161,
					0.7196895143307529
				],
				[
					-0.7196986656795161,
					0.9595829686580828
				],
				[
					-0.7196986656795161,
					1.4393790286615058
				],
				[
					-0.7196986656795161,
					1.6792724829889494
				],
				[
					-0.7196986656795161,
					2.1590685429923724
				],
				[
					-0.23991175702474266,
					2.1590685429923724
				],
				[
					0,
					2.1590685429923724
				],
				[
					0,
					2.398971148668352
				],
				[
					0.23991175702462897,
					2.6388646029957954
				],
				[
					0.7196986656794024,
					2.6388646029957954
				],
				[
					0.9595738173094333,
					2.6388646029957954
				],
				[
					0.9595738173094333,
					3.1186606629992184
				],
				[
					1.4393973313589186,
					3.1186606629992184
				],
				[
					1.6792724829888357,
					3.3585541173265483
				],
				[
					2.159059391643609,
					3.8383501773299713
				],
				[
					2.398971148668352,
					3.8383501773299713
				],
				[
					2.6388829056930945,
					4.078243631657301
				],
				[
					3.118669814347868,
					4.078243631657301
				],
				[
					3.3585449659778988,
					4.078243631657301
				],
				[
					3.8383684800272704,
					4.078243631657301
				],
				[
					4.078243631657301,
					4.078243631657301
				],
				[
					4.558030540312075,
					4.078243631657301
				],
				[
					4.797942297336817,
					4.078243631657301
				],
				[
					5.03785405436156,
					4.078243631657301
				],
				[
					5.51764096301622,
					4.078243631657301
				],
				[
					5.757516114646251,
					4.078243631657301
				],
				[
					6.237339628695736,
					4.078243631657301
				],
				[
					6.237339628695736,
					3.5984567230026414
				],
				[
					6.237339628695736,
					3.3585541173265483
				],
				[
					6.237339628695736,
					2.8787580573231253
				],
				[
					6.237339628695736,
					2.6388646029957954
				],
				[
					6.237339628695736,
					2.398971148668352
				],
				[
					6.237339628695736,
					1.9191750886649288
				],
				[
					6.237339628695736,
					1.6792724829889494
				],
				[
					5.997427871670993,
					1.199485574334176
				],
				[
					5.997427871670993,
					0.9595829686580828
				],
				[
					5.997427871670993,
					0.4797869086546598
				],
				[
					5.757516114646251,
					0.4797869086546598
				],
				[
					5.757516114646251,
					0.2398934543273299
				],
				[
					5.757516114646251,
					0
				],
				[
					5.277729205991591,
					0
				],
				[
					5.277729205991591,
					-0.479796060003423
				],
				[
					5.03785405436156,
					-0.7196986656795161
				],
				[
					5.03785405436156,
					-1.1994855743342896
				],
				[
					4.797942297336817,
					-1.1994855743342896
				],
				[
					4.797942297336817,
					-1.439388180010269
				],
				[
					4.318155388682044,
					-1.439388180010269
				],
				[
					4.318155388682044,
					-1.919184240013692
				],
				[
					4.078243631657301,
					-1.919184240013692
				],
				[
					4.078243631657301,
					-2.159077694341022
				],
				[
					3.5984567230025277,
					-2.159077694341022
				],
				[
					3.3585449659778988,
					-2.159077694341022
				],
				[
					2.8787580573231253,
					-2.3989711486684655
				],
				[
					2.6388829056930945,
					-2.3989711486684655
				],
				[
					2.398971148668352,
					-2.3989711486684655
				],
				[
					1.919184240013692,
					-2.3989711486684655
				],
				[
					1.6792724829888357,
					-2.8787672086718885
				],
				[
					1.199485574334176,
					-2.8787672086718885
				],
				[
					0.9595738173094333,
					-2.8787672086718885
				],
				[
					0.4797869086546598,
					-2.8787672086718885
				],
				[
					0.4797869086546598,
					-2.6388737543445586
				],
				[
					0.23991175702462897,
					-2.6388737543445586
				],
				[
					0,
					-2.6388737543445586
				],
				[
					0,
					-2.3989711486684655
				],
				[
					-0.47978690865477347,
					-2.3989711486684655
				],
				[
					-0.7196986656795161,
					-2.3989711486684655
				],
				[
					-0.7196986656795161,
					-2.159077694341022
				],
				[
					-0.7196986656795161,
					-1.6792816343377126
				],
				[
					-1.1994855743342896,
					-1.6792816343377126
				],
				[
					-1.1994855743342896,
					-1.439388180010269
				],
				[
					-1.1994855743342896,
					-0.959592120006846
				],
				[
					-1.1994855743342896,
					-0.7196986656795161
				],
				[
					-1.1994855743342896,
					-0.23990260567609312
				],
				[
					-0.9595738173095469,
					-0.23990260567609312
				],
				[
					-0.7196986656795161,
					-0.23990260567609312
				],
				[
					-0.7196986656795161,
					-0.23990260567609312
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 160,
			"versionNonce": 1350235859,
			"isDeleted": false,
			"id": "ZbD7Ly06chxNo3oAoy8LH",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 612.2850871025975,
			"y": 526.5044861774927,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 2.6388829056930945,
			"height": 10.55547671468048,
			"seed": 1767322664,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.479796060003423
				],
				[
					0,
					-0.7196986656795161
				],
				[
					0,
					-1.199485574334176
				],
				[
					0,
					-1.439388180010269
				],
				[
					0,
					-1.679281634337599
				],
				[
					0,
					-2.159077694341022
				],
				[
					0,
					-2.3989711486684655
				],
				[
					0,
					-2.8787672086718885
				],
				[
					0,
					-3.118669814347868
				],
				[
					0,
					-3.5984567230026414
				],
				[
					0,
					-3.8383593286787345
				],
				[
					-0.23991175702474266,
					-4.558048843009487
				],
				[
					-0.23991175702474266,
					-4.797942297336817
				],
				[
					-0.7196986656794024,
					-5.27773835734024
				],
				[
					-0.7196986656794024,
					-5.5176409630163334
				],
				[
					-0.7196986656794024,
					-5.757534417343663
				],
				[
					-0.9596104227042588,
					-5.757534417343663
				],
				[
					-0.9596104227042588,
					-6.477223931674416
				],
				[
					-1.4393973313589186,
					-6.477223931674416
				],
				[
					-1.4393973313589186,
					-6.957019991677953
				],
				[
					-1.4393973313589186,
					-7.196913446005283
				],
				[
					-1.4393973313589186,
					-7.676709506008706
				],
				[
					-1.6793090883836612,
					-7.916612111684685
				],
				[
					-1.6793090883836612,
					-8.156505566012129
				],
				[
					-2.1590959970384347,
					-8.636301626015552
				],
				[
					-2.1590959970384347,
					-8.876195080342882
				],
				[
					-2.1590959970384347,
					-9.355991140346305
				],
				[
					-2.3989711486684655,
					-9.355991140346305
				],
				[
					-2.3989711486684655,
					-9.595884594673635
				],
				[
					-2.6388829056930945,
					-10.075680654677058
				],
				[
					-2.6388829056930945,
					-10.31558326035315
				],
				[
					-2.6388829056930945,
					-10.55547671468048
				],
				[
					-2.6388829056930945,
					-10.55547671468048
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 162,
			"versionNonce": 1106432989,
			"isDeleted": false,
			"id": "YBex1EFsozw2MuYcO6OsV",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 608.4467186225701,
			"y": 515.4692134028088,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 5.997427871670993,
			"height": 2.1590685429923724,
			"seed": 1753490728,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.23990260567597943
				],
				[
					-0.23991175702474266,
					0.23990260567597943
				],
				[
					-0.23991175702474266,
					0.479796060003423
				],
				[
					-0.7196986656794024,
					0.479796060003423
				],
				[
					-0.7196986656794024,
					1.199485574334176
				],
				[
					-0.7196986656794024,
					1.439388180010269
				],
				[
					-0.7196986656794024,
					1.9191750886649288
				],
				[
					-0.9595738173094333,
					1.9191750886649288
				],
				[
					-0.9595738173094333,
					1.679281634337599
				],
				[
					-0.47978690865477347,
					1.439388180010269
				],
				[
					-0.23991175702474266,
					0.959592120006846
				],
				[
					-0.23991175702474266,
					0.7196895143307529
				],
				[
					-0.23991175702474266,
					0.479796060003423
				],
				[
					0.23991175702474266,
					0.479796060003423
				],
				[
					0.23991175702474266,
					0
				],
				[
					0.23991175702474266,
					-0.23989345432744358
				],
				[
					0.47978690865477347,
					-0.23989345432744358
				],
				[
					0.9595738173095469,
					-0.23989345432744358
				],
				[
					1.1994855743342896,
					-0.23989345432744358
				],
				[
					1.4393973313589186,
					-0.23989345432744358
				],
				[
					1.4393973313589186,
					0.23990260567597943
				],
				[
					1.919184240013692,
					0.23990260567597943
				],
				[
					1.919184240013692,
					0.479796060003423
				],
				[
					2.159059391643723,
					0.479796060003423
				],
				[
					2.638882905693208,
					0.7196895143307529
				],
				[
					2.8787580573231253,
					0.7196895143307529
				],
				[
					3.3585449659778988,
					0.7196895143307529
				],
				[
					3.3585449659778988,
					1.199485574334176
				],
				[
					3.5984567230026414,
					1.199485574334176
				],
				[
					3.838368480027384,
					1.199485574334176
				],
				[
					4.3181553886821575,
					1.439388180010269
				],
				[
					4.558030540312188,
					1.439388180010269
				],
				[
					5.03785405436156,
					1.439388180010269
				],
				[
					5.03785405436156,
					1.9191750886649288
				],
				[
					5.03785405436156,
					1.9191750886649288
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 166,
			"versionNonce": 708486259,
			"isDeleted": false,
			"id": "HH6fEodpcc1wkHyi3LLwX",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 605.2442719755762,
			"y": 500.1998818133533,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 4.808015201697458,
			"height": 8.626138891606388,
			"seed": 1694456360,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.28281998114493945,
					0
				],
				[
					0.4242299717172955,
					0
				],
				[
					0.7070607417529118,
					0
				],
				[
					0.8484707323252678,
					-0.14140999057246972
				],
				[
					0.9898807228977375,
					-0.4242299717172955
				],
				[
					1.4141214835057099,
					-0.5656507511804421
				],
				[
					1.6969414646505356,
					-0.8484707323252678
				],
				[
					1.8383514552230054,
					-0.9898807228976807
				],
				[
					2.121182225258508,
					-1.2727114929332402
				],
				[
					2.4040022064033337,
					-1.4141214835057099
				],
				[
					2.68683297643895,
					-1.8383514552229485
				],
				[
					2.828242967011306,
					-1.979772234686095
				],
				[
					3.1110629481562455,
					-2.262592215830921
				],
				[
					3.2524729387286015,
					-2.686832976438893
				],
				[
					3.393893718191748,
					-2.828242967011306
				],
				[
					3.676713699336574,
					-2.969652957583776
				],
				[
					3.676713699336574,
					-3.2524729387286015
				],
				[
					3.8181236899090436,
					-3.2524729387286015
				],
				[
					4.100954459944546,
					-3.8181236899090436
				],
				[
					4.242364450517016,
					-3.9595336804814565
				],
				[
					4.525184431661842,
					-4.383774441089429
				],
				[
					4.525184431661842,
					-4.666594422234255
				],
				[
					4.666594422234311,
					-4.808015201697401
				],
				[
					4.666594422234311,
					-5.090835182842284
				],
				[
					4.808015201697458,
					-5.232250567860035
				],
				[
					4.808015201697458,
					-5.373660558432448
				],
				[
					4.808015201697458,
					-5.656485934022669
				],
				[
					4.808015201697458,
					-5.797895924595082
				],
				[
					4.808015201697458,
					-6.080721300185303
				],
				[
					4.808015201697458,
					-6.222131290757716
				],
				[
					4.808015201697458,
					-6.50495666634788
				],
				[
					4.808015201697458,
					-6.646372051365688
				],
				[
					4.808015201697458,
					-6.787782041938101
				],
				[
					4.808015201697458,
					-7.070607417528322
				],
				[
					4.808015201697458,
					-7.212017408100735
				],
				[
					4.808015201697458,
					-7.494842783690956
				],
				[
					4.808015201697458,
					-7.636252774263369
				],
				[
					4.808015201697458,
					-7.77766815928112
				],
				[
					4.808015201697458,
					-8.060493534871341
				],
				[
					4.808015201697458,
					-8.201903525443754
				],
				[
					4.808015201697458,
					-8.484728901033975
				],
				[
					4.808015201697458,
					-8.626138891606388
				],
				[
					4.808015201697458,
					-8.626138891606388
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 159,
			"versionNonce": 663113789,
			"isDeleted": false,
			"id": "QiOIEfGPpt_HORRszrb3Y",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 608.7795756843404,
			"y": 482.6647786545503,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 2.121182225258508,
			"height": 5.090840577287565,
			"seed": 721189672,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.1414153850177513
				],
				[
					0.28281998114482576,
					-0.1414153850177513
				],
				[
					0.4242299717172955,
					-0.1414153850177513
				],
				[
					0.7070607417527981,
					-0.1414153850177513
				],
				[
					0.7070607417527981,
					-0.42424076060797233
				],
				[
					0.8484707323252678,
					-0.42424076060797233
				],
				[
					1.1312907134700936,
					-0.42424076060797233
				],
				[
					1.1312907134700936,
					-0.5656507511803852
				],
				[
					1.2727114929332402,
					-0.5656507511803852
				],
				[
					1.4141214835055962,
					-0.8484761267706062
				],
				[
					1.4141214835055962,
					-0.9898861173430191
				],
				[
					1.6969414646505356,
					-0.9898861173430191
				],
				[
					1.6969414646505356,
					-1.1313015023608273
				],
				[
					1.8383514552228917,
					-1.1313015023608273
				],
				[
					2.121182225258508,
					-1.414121483505653
				],
				[
					2.121182225258508,
					-1.5555368685234043
				],
				[
					1.9797722346860382,
					-1.5555368685234043
				],
				[
					1.8383514552228917,
					-1.5555368685234043
				],
				[
					1.8383514552228917,
					-1.2727114929332402
				],
				[
					1.8383514552228917,
					-1.1313015023608273
				],
				[
					1.8383514552228917,
					-0.9898861173430191
				],
				[
					1.8383514552228917,
					-0.7070607417527981
				],
				[
					1.8383514552228917,
					-0.1414153850177513
				],
				[
					1.8383514552228917,
					0.2828199811448826
				],
				[
					1.8383514552228917,
					0.7070607417528549
				],
				[
					1.8383514552228917,
					0.8484707323252678
				],
				[
					1.8383514552228917,
					1.2727060984879017
				],
				[
					1.8383514552228917,
					1.414121483505653
				],
				[
					1.8383514552228917,
					1.838356849668287
				],
				[
					1.8383514552228917,
					2.121182225258508
				],
				[
					1.8383514552228917,
					2.262592215830921
				],
				[
					1.8383514552228917,
					2.545417591421142
				],
				[
					1.8383514552228917,
					2.6868275819935548
				],
				[
					1.8383514552228917,
					2.828242967011363
				],
				[
					1.8383514552228917,
					3.1110629481561887
				],
				[
					1.8383514552228917,
					3.25247833317394
				],
				[
					1.8383514552228917,
					3.535303708764161
				],
				[
					1.8383514552228917,
					3.535303708764161
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 156,
			"versionNonce": 921935379,
			"isDeleted": false,
			"id": "iikbLGuh-vRFSow6t02-2",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 612.08181203666,
			"y": 476.09873900387606,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 6.142153321540945,
			"height": 18.70567682982346,
			"seed": 553098024,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.27919556475671925
				],
				[
					0.5583698290696475,
					-0.27919556475671925
				],
				[
					0.5583698290696475,
					-0.8375653938263667
				],
				[
					0.8375334431608508,
					-0.8375653938263667
				],
				[
					1.116739658139295,
					-1.1167609585830292
				],
				[
					1.6751094872090562,
					-1.6751414378745721
				],
				[
					1.6751094872090562,
					-1.954326352409339
				],
				[
					1.9543157021873867,
					-1.954326352409339
				],
				[
					2.512685531257148,
					-2.2335112669442196
				],
				[
					2.791891746235706,
					-2.791891746235706
				],
				[
					2.791891746235706,
					-3.6294571400620725
				],
				[
					3.3502615753052396,
					-3.6294571400620725
				],
				[
					3.6294251893965566,
					-3.908652704818735
				],
				[
					3.6294251893965566,
					-4.467033184110221
				],
				[
					3.908631404375001,
					-4.746218098645045
				],
				[
					3.908631404375001,
					-5.025403013179925
				],
				[
					3.908631404375001,
					-5.583783492471412
				],
				[
					4.467001233444762,
					-5.862979057228074
				],
				[
					4.467001233444762,
					-6.4213488862977215
				],
				[
					4.7462074484230925,
					-6.700544451054384
				],
				[
					4.7462074484230925,
					-7.25892493034587
				],
				[
					5.304577277492854,
					-7.538109844880751
				],
				[
					5.304577277492854,
					-7.817294759415574
				],
				[
					5.304577277492854,
					-8.37567523870706
				],
				[
					5.304577277492854,
					-8.654870803463723
				],
				[
					5.304577277492854,
					-9.213240632533427
				],
				[
					5.304577277492854,
					-9.49243619729009
				],
				[
					5.304577277492854,
					-10.050816676581576
				],
				[
					5.304577277492854,
					-10.3300015911164
				],
				[
					5.304577277492854,
					-10.60918650565128
				],
				[
					5.304577277492854,
					-11.167566984942766
				],
				[
					5.304577277492854,
					-11.446762549699429
				],
				[
					5.304577277492854,
					-12.284327943525739
				],
				[
					5.304577277492854,
					-13.121893337352105
				],
				[
					5.583783492471298,
					-13.959458731178415
				],
				[
					5.583783492471298,
					-14.797024125004782
				],
				[
					6.142153321540945,
					-15.355404604296268
				],
				[
					6.142153321540945,
					-15.913785083587754
				],
				[
					6.142153321540945,
					-16.75135047741412
				],
				[
					5.862947106562501,
					-17.030546042170783
				],
				[
					5.862947106562501,
					-17.868111435997093
				],
				[
					5.862947106562501,
					-18.147296350531974
				],
				[
					5.862947106562501,
					-18.70567682982346
				],
				[
					5.862947106562501,
					-18.70567682982346
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 144,
			"versionNonce": 439042205,
			"isDeleted": false,
			"id": "3LaW9cp_0F85TFvWCTqE2",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 617.9447591432225,
			"y": 457.6722470885875,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 5.304577277492854,
			"height": 4.187837619353502,
			"seed": 2096026920,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.27916361409120327,
					0
				],
				[
					-0.27916361409120327,
					0.27919556475660556
				],
				[
					-0.8375760440482054,
					0.5583804792914862
				],
				[
					-1.1167396581394087,
					1.395945873117796
				],
				[
					-1.6751094872090562,
					1.954326352409339
				],
				[
					-1.9543157021875004,
					2.791891746235649
				],
				[
					-2.2335219171659446,
					3.0710873109923114
				],
				[
					-2.2335219171659446,
					3.350272225527135
				],
				[
					-2.791891746235592,
					3.350272225527135
				],
				[
					-2.791891746235592,
					3.908652704818678
				],
				[
					-2.791891746235592,
					4.187837619353502
				],
				[
					-3.0710553603267954,
					4.187837619353502
				],
				[
					-3.0710553603267954,
					3.6294677902837975
				],
				[
					-2.5126855312572616,
					3.6294677902837975
				],
				[
					-2.2335219171659446,
					3.350272225527135
				],
				[
					-1.9543157021875004,
					3.0710873109923114
				],
				[
					-1.1167396581394087,
					2.512706831700825
				],
				[
					-1.1167396581394087,
					2.2335219171659446
				],
				[
					-0.5583698290696475,
					2.2335219171659446
				],
				[
					-0.5583698290696475,
					1.6751414378744585
				],
				[
					-0.27916361409120327,
					1.6751414378744585
				],
				[
					0.2792062149784442,
					1.395945873117796
				],
				[
					0.5583698290696475,
					1.395945873117796
				],
				[
					0.8375760440482054,
					1.395945873117796
				],
				[
					0.8375760440482054,
					1.954326352409339
				],
				[
					1.395945873117853,
					1.954326352409339
				],
				[
					1.395945873117853,
					2.2335219171659446
				],
				[
					1.6751520880962971,
					2.791891746235649
				],
				[
					1.6751520880962971,
					3.0710873109923114
				],
				[
					1.6751520880962971,
					3.350272225527135
				],
				[
					2.2335219171660583,
					3.350272225527135
				],
				[
					2.2335219171660583,
					3.350272225527135
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 122,
			"versionNonce": 1637639091,
			"isDeleted": false,
			"id": "0vf9mP2dU_eGNgdSXCTU6",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 621.0158571044367,
			"y": 459.0681929617053,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 1.954315702187614,
			"height": 1.6751414378745153,
			"seed": 1514867496,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.558380479291543
				],
				[
					0.27916361409120327,
					0.558380479291543
				],
				[
					0.27916361409120327,
					0.8375760440481486
				],
				[
					0.8375760440480917,
					0.8375760440481486
				],
				[
					0.8375760440480917,
					1.395945873117853
				],
				[
					1.1167396581394087,
					1.395945873117853
				],
				[
					1.1167396581394087,
					1.6751414378745153
				],
				[
					1.6751094872090562,
					1.6751414378745153
				],
				[
					1.954315702187614,
					1.6751414378745153
				],
				[
					1.954315702187614,
					1.6751414378745153
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 161,
			"versionNonce": 1603478781,
			"isDeleted": false,
			"id": "1iJnMEhvWMU7u2strPIVH",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 633.5793699624973,
			"y": 443.6429974538862,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 17.868090135553416,
			"height": 15.076219689761388,
			"seed": 1872636968,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.5583698290696475,
					-0.27919556475660556
				],
				[
					0.8375760440482054,
					-0.27919556475660556
				],
				[
					1.395945873117853,
					-0.27919556475660556
				],
				[
					1.395945873117853,
					-0.8375653938263099
				],
				[
					1.6751094872090562,
					-0.8375653938263099
				],
				[
					1.9543157021875004,
					-0.8375653938263099
				],
				[
					2.5126855312572616,
					-0.8375653938263099
				],
				[
					2.791891746235706,
					-0.8375653938263099
				],
				[
					3.3502615753053533,
					-0.8375653938263099
				],
				[
					3.3502615753053533,
					-1.1167609585829723
				],
				[
					3.629467790283911,
					-1.1167609585829723
				],
				[
					4.187837619353445,
					-1.1167609585829723
				],
				[
					4.467001233444762,
					-1.1167609585829723
				],
				[
					5.304577277492967,
					-1.6751414378744585
				],
				[
					5.583783492471298,
					-1.6751414378744585
				],
				[
					6.421359536519503,
					-1.954326352409339
				],
				[
					6.70052315061082,
					-2.233511266944163
				],
				[
					7.258892979680354,
					-2.791891746235649
				],
				[
					7.538099194658912,
					-2.791891746235649
				],
				[
					8.09646902372856,
					-3.0710873109923114
				],
				[
					8.375675238707004,
					-3.0710873109923114
				],
				[
					8.934045067776765,
					-3.629457140061959
				],
				[
					9.213251282755209,
					-4.467033184110164
				],
				[
					10.05078472591606,
					-4.746218098644988
				],
				[
					10.329990940894618,
					-5.025403013179812
				],
				[
					10.888360769964265,
					-5.583783492471298
				],
				[
					11.16756698494271,
					-5.862979057228017
				],
				[
					11.72593681401247,
					-6.421348886297665
				],
				[
					12.005143028990801,
					-6.700544451054327
				],
				[
					12.005143028990801,
					-7.25892493034587
				],
				[
					12.284306643082118,
					-7.538109844880637
				],
				[
					12.842676472151766,
					-7.8172947594155175
				],
				[
					13.121882687130324,
					-8.375675238707004
				],
				[
					13.680252516199857,
					-8.654870803463666
				],
				[
					13.959458731178415,
					-9.492436197289976
				],
				[
					14.797034775226507,
					-10.330001591116343
				],
				[
					15.07619838931771,
					-11.16756698494271
				],
				[
					15.634568218387471,
					-11.446762549699315
				],
				[
					15.913774433365916,
					-12.005132378769076
				],
				[
					16.472144262435563,
					-12.284327943525682
				],
				[
					16.472144262435563,
					-12.563512858060562
				],
				[
					16.75135047741412,
					-13.121893337352049
				],
				[
					17.030514091505324,
					-13.401078251886872
				],
				[
					17.030514091505324,
					-13.959458731178358
				],
				[
					17.588926521462213,
					-14.23865429593502
				],
				[
					17.588926521462213,
					-14.797024125004725
				],
				[
					17.868090135553416,
					-14.797024125004725
				],
				[
					17.868090135553416,
					-15.076219689761388
				],
				[
					17.868090135553416,
					-15.076219689761388
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 170,
			"versionNonce": 1918596435,
			"isDeleted": false,
			"id": "mWpvxteEgla8Ts10xeveY",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 653.4017758002383,
			"y": 421.8662439632923,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 9.213251282755095,
			"height": 8.654860153241884,
			"seed": 54185256,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.27916361409120327,
					-0.5583804792914862
				],
				[
					-0.27916361409120327,
					-0.8375760440481486
				],
				[
					-0.27916361409120327,
					-1.1167609585829723
				],
				[
					0,
					-1.1167609585829723
				],
				[
					0.5584124299568884,
					-1.6751414378744585
				],
				[
					0.8375760440480917,
					-1.954326352409339
				],
				[
					1.395945873117853,
					-2.512706831700825
				],
				[
					1.6751520880961834,
					-2.512706831700825
				],
				[
					2.2335219171659446,
					-2.791891746235649
				],
				[
					2.512728132144389,
					-3.350272225527135
				],
				[
					2.791891746235706,
					-3.350272225527135
				],
				[
					3.3503041761925942,
					-3.6294677902837975
				],
				[
					3.6294677902837975,
					-3.6294677902837975
				],
				[
					4.187837619353445,
					-3.908652704818678
				],
				[
					4.467043834331889,
					-3.908652704818678
				],
				[
					4.746250049310447,
					-3.908652704818678
				],
				[
					5.304619878380095,
					-3.908652704818678
				],
				[
					5.583783492471298,
					-3.908652704818678
				],
				[
					6.1421959224283,
					-3.908652704818678
				],
				[
					6.1421959224283,
					-3.6294677902837975
				],
				[
					6.1421959224283,
					-3.0710873109923114
				],
				[
					6.1421959224283,
					-2.791891746235649
				],
				[
					6.1421959224283,
					-2.2335219171659446
				],
				[
					5.862989707449742,
					-1.954326352409339
				],
				[
					5.862989707449742,
					-1.395945873117853
				],
				[
					5.583783492471298,
					-0.8375760440481486
				],
				[
					5.02541366340165,
					-0.27919556475660556
				],
				[
					5.02541366340165,
					0
				],
				[
					4.467043834331889,
					0.5583698290697043
				],
				[
					4.467043834331889,
					0.8375653938263667
				],
				[
					4.467043834331889,
					1.395945873117853
				],
				[
					3.9086740052622417,
					1.6751307876527335
				],
				[
					3.6294677902837975,
					1.9543157021875572
				],
				[
					3.0710979612140363,
					2.5126961814790434
				],
				[
					2.791891746235706,
					2.791891746235706
				],
				[
					2.512728132144389,
					3.3502615753053533
				],
				[
					1.9543583030747413,
					3.6294571400620725
				],
				[
					1.9543583030747413,
					3.9086420545968963
				],
				[
					1.6751520880961834,
					4.467022533888382
				],
				[
					1.1167822590266496,
					4.467022533888382
				],
				[
					1.1167822590266496,
					4.746207448423206
				],
				[
					0.8375760440480917,
					4.746207448423206
				],
				[
					1.395945873117853,
					4.746207448423206
				],
				[
					1.6751520880961834,
					4.746207448423206
				],
				[
					2.512728132144389,
					4.746207448423206
				],
				[
					2.791891746235706,
					4.746207448423206
				],
				[
					3.6294677902837975,
					4.746207448423206
				],
				[
					4.467043834331889,
					4.746207448423206
				],
				[
					5.304619878380095,
					4.746207448423206
				],
				[
					5.583783492471298,
					4.746207448423206
				],
				[
					6.1421959224283,
					4.746207448423206
				],
				[
					6.421359536519503,
					4.746207448423206
				],
				[
					7.258935580567595,
					4.746207448423206
				],
				[
					7.538141795546153,
					4.746207448423206
				],
				[
					8.096511624615687,
					4.746207448423206
				],
				[
					8.375675238707004,
					4.746207448423206
				],
				[
					8.934087668663892,
					4.746207448423206
				],
				[
					8.934087668663892,
					4.746207448423206
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 146,
			"versionNonce": 188710237,
			"isDeleted": false,
			"id": "Ul8kgfhwik8m3khAm6Xkk",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 663.1733969120631,
			"y": 417.9575912584736,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 5.862989707449856,
			"height": 10.330001591116343,
			"seed": 31154472,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.5583804792914862
				],
				[
					0.2792062149784442,
					-0.8375653938263099
				],
				[
					0.5584124299568884,
					-0.8375653938263099
				],
				[
					1.116782259026536,
					-0.8375653938263099
				],
				[
					1.3959458731177392,
					-1.395945873117796
				],
				[
					1.9543583030747413,
					-1.395945873117796
				],
				[
					2.2335219171659446,
					-1.6751307876526766
				],
				[
					2.791891746235592,
					-1.6751307876526766
				],
				[
					3.07109796121415,
					-1.954326352409339
				],
				[
					3.3503041761925942,
					-1.954326352409339
				],
				[
					3.3503041761925942,
					-2.512706831700825
				],
				[
					3.9086740052622417,
					-2.791891746235649
				],
				[
					4.187837619353445,
					-3.350272225527135
				],
				[
					4.187837619353445,
					-3.6294571400620157
				],
				[
					4.746250049310447,
					-3.6294571400620157
				],
				[
					4.746250049310447,
					-4.187837619353502
				],
				[
					5.02541366340165,
					-4.467022533888326
				],
				[
					5.02541366340165,
					-4.746218098644988
				],
				[
					5.02541366340165,
					-5.304598577936474
				],
				[
					5.304619878380095,
					-5.304598577936474
				],
				[
					5.304619878380095,
					-5.583783492471355
				],
				[
					5.862989707449856,
					-6.142163971762841
				],
				[
					5.862989707449856,
					-6.421348886297665
				],
				[
					5.862989707449856,
					-6.979729365589151
				],
				[
					5.862989707449856,
					-7.258914280124031
				],
				[
					5.862989707449856,
					-7.538109844880637
				],
				[
					5.862989707449856,
					-8.09649032417218
				],
				[
					5.862989707449856,
					-8.375675238707004
				],
				[
					5.862989707449856,
					-8.93405571799849
				],
				[
					5.862989707449856,
					-9.21324063253337
				],
				[
					5.862989707449856,
					-9.771621111824857
				],
				[
					5.862989707449856,
					-10.05080602635968
				],
				[
					5.862989707449856,
					-10.330001591116343
				],
				[
					5.862989707449856,
					-10.330001591116343
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 153,
			"versionNonce": 1753699059,
			"isDeleted": false,
			"id": "Ulu1_fg3HroVJSKY_fWwH",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 663.8748246000757,
			"y": 408.8642112540635,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 8.050957662318183,
			"height": 2.8983435299558664,
			"seed": 272759080,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3220333925781915,
					-0.1610228386822996
				],
				[
					0.48305008886723044,
					-0.1610228386822996
				],
				[
					0.6440790699427907,
					-0.1610228386822996
				],
				[
					0.6440790699427907,
					-0.3220395349713385
				],
				[
					0.9661124625208686,
					-0.3220395349713385
				],
				[
					0.9661124625208686,
					-0.4830562312604343
				],
				[
					1.1271291588100212,
					-0.4830562312604343
				],
				[
					1.4491748361746204,
					-0.4830562312604343
				],
				[
					1.6101915324636593,
					-0.8050957662317728
				],
				[
					1.9322249250418508,
					-0.8050957662317728
				],
				[
					2.0932416213308898,
					-0.9661186049141293
				],
				[
					2.25427060240645,
					-0.9661186049141293
				],
				[
					2.576303994984528,
					-1.288151997492264
				],
				[
					2.7373206912736805,
					-1.288151997492264
				],
				[
					3.0593663686382797,
					-1.4491748361745636
				],
				[
					3.2203830649273186,
					-1.771214371145959
				],
				[
					3.5424164575053965,
					-1.9322310674349978
				],
				[
					3.703433153794549,
					-1.9322310674349978
				],
				[
					3.8644621348701094,
					-2.0932477637240368
				],
				[
					4.186495527448187,
					-2.0932477637240368
				],
				[
					4.347512223737226,
					-2.415287298695432
				],
				[
					4.669557901101825,
					-2.415287298695432
				],
				[
					4.669557901101825,
					-2.5763101373777317
				],
				[
					4.830574597390978,
					-2.5763101373777317
				],
				[
					4.830574597390978,
					-2.8983435299558664
				],
				[
					4.991591293680017,
					-2.8983435299558664
				],
				[
					5.313624686258208,
					-2.7373268336668275
				],
				[
					5.474653667333655,
					-2.5763101373777317
				],
				[
					5.7966870599118465,
					-2.254270602406393
				],
				[
					5.957703756200885,
					-2.0932477637240368
				],
				[
					6.279749433565485,
					-2.0932477637240368
				],
				[
					6.440766129854637,
					-1.9322310674349978
				],
				[
					6.601782826143676,
					-1.6101915324636025
				],
				[
					6.923816218721754,
					-1.6101915324636025
				],
				[
					6.923816218721754,
					-1.4491748361745636
				],
				[
					7.084845199797314,
					-1.1271353012031682
				],
				[
					7.406878592375506,
					-1.1271353012031682
				],
				[
					7.567895288664545,
					-0.9661186049141293
				],
				[
					7.567895288664545,
					-0.6440790699427339
				],
				[
					7.889940966029144,
					-0.6440790699427339
				],
				[
					8.050957662318183,
					-0.6440790699427339
				],
				[
					8.050957662318183,
					-0.6440790699427339
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 127,
			"versionNonce": 1149356477,
			"isDeleted": false,
			"id": "d0g7CFvdc2CX-SGbwaxZo",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 621.2047489897893,
			"y": 459.4242278303791,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 2.0932539061172974,
			"height": 2.0932539061173543,
			"seed": 534447912,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.32204567736465606
				],
				[
					-0.3220456773645992,
					-0.32204567736465606
				],
				[
					-0.3220456773645992,
					-0.483062373653695
				],
				[
					-0.48306237365363813,
					-0.483062373653695
				],
				[
					-0.48306237365363813,
					-0.8050957662318297
				],
				[
					-0.8050957662318297,
					-0.8050957662318297
				],
				[
					-0.8050957662318297,
					-0.9661124625209254
				],
				[
					-0.9661124625208686,
					-0.9661124625209254
				],
				[
					-1.1271414435964289,
					-1.1271414435964289
				],
				[
					-1.4491748361745067,
					-1.4491748361746204
				],
				[
					-1.6101915324636593,
					-1.4491748361746204
				],
				[
					-1.6101915324636593,
					-1.6101915324636593
				],
				[
					-1.9322372098282585,
					-1.6101915324636593
				],
				[
					-1.9322372098282585,
					-1.9322372098282585
				],
				[
					-2.0932539061172974,
					-1.9322372098282585
				],
				[
					-2.0932539061172974,
					-2.0932539061173543
				],
				[
					-2.0932539061172974,
					-2.0932539061173543
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 150,
			"versionNonce": 346455187,
			"isDeleted": false,
			"id": "mfAEYQw-frUB0GpJtEYRn",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 643.2643680706266,
			"y": 494.0433457783473,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 4.669557901101825,
			"height": 8.211974358607279,
			"seed": 1651648552,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.3220456773645992
				],
				[
					0,
					-0.483062373653695
				],
				[
					-0.32203339257807784,
					-0.483062373653695
				],
				[
					-0.32203339257807784,
					-0.6440790699427907
				],
				[
					-0.48305008886723044,
					-0.6440790699427907
				],
				[
					-0.8050957662318297,
					-0.9661124625208686
				],
				[
					-0.9661124625208686,
					-1.1271414435964289
				],
				[
					-1.1271291588099075,
					-1.4491748361745636
				],
				[
					-1.4491748361745067,
					-1.6101915324636593
				],
				[
					-1.6101915324636593,
					-1.9322372098282585
				],
				[
					-1.9322249250417372,
					-2.0932539061172974
				],
				[
					-2.093241621330776,
					-2.254270602406393
				],
				[
					-2.093241621330776,
					-2.576303994984528
				],
				[
					-2.2542706024063364,
					-2.737332976060088
				],
				[
					-2.2542706024063364,
					-3.2203830649273186
				],
				[
					-2.576303994984528,
					-3.542428742291918
				],
				[
					-2.576303994984528,
					-3.7034454385809568
				],
				[
					-2.576303994984528,
					-3.8644621348700525
				],
				[
					-2.576303994984528,
					-4.186495527448187
				],
				[
					-2.576303994984528,
					-4.3475245085237475
				],
				[
					-2.576303994984528,
					-4.669557901101825
				],
				[
					-2.737320691273567,
					-4.830574597390921
				],
				[
					-2.737320691273567,
					-5.15262027475552
				],
				[
					-3.059366368638166,
					-5.313636971044616
				],
				[
					-3.059366368638166,
					-5.474653667333655
				],
				[
					-3.220383064927205,
					-5.7966870599118465
				],
				[
					-3.5424164575053965,
					-5.95771604098735
				],
				[
					-3.5424164575053965,
					-6.279749433565485
				],
				[
					-3.7034331537944354,
					-6.44076612985458
				],
				[
					-3.8644621348699957,
					-6.601782826143619
				],
				[
					-3.8644621348699957,
					-6.923828503508275
				],
				[
					-4.186495527448187,
					-6.923828503508275
				],
				[
					-4.186495527448187,
					-7.084845199797314
				],
				[
					-4.347512223737226,
					-7.406878592375449
				],
				[
					-4.347512223737226,
					-7.567907573451009
				],
				[
					-4.347512223737226,
					-7.889940966029144
				],
				[
					-4.669557901101825,
					-7.889940966029144
				],
				[
					-4.669557901101825,
					-8.050957662318183
				],
				[
					-4.669557901101825,
					-8.211974358607279
				],
				[
					-4.669557901101825,
					-8.211974358607279
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 145,
			"versionNonce": 1283164701,
			"isDeleted": false,
			"id": "evQG-VVFaz1qfaDQS4EbY",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 632.1540440396702,
			"y": 478.5855095236537,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 1.6101915324636593,
			"height": 6.44076612985458,
			"seed": 2086869544,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3220456773645992,
					0
				],
				[
					0.48306237365363813,
					0
				],
				[
					0.8050957662318297,
					0
				],
				[
					0.9661247473072763,
					0
				],
				[
					0.9661247473072763,
					-0.1610289810755603
				],
				[
					0.9661247473072763,
					-0.483062373653695
				],
				[
					1.2881581398854678,
					-0.483062373653695
				],
				[
					1.2881581398854678,
					-0.6440790699427339
				],
				[
					1.4491748361745067,
					-0.6440790699427339
				],
				[
					1.4491748361745067,
					-0.96612474730739
				],
				[
					1.6101915324636593,
					-0.96612474730739
				],
				[
					1.6101915324636593,
					-0.8050957662318297
				],
				[
					1.6101915324636593,
					-0.6440790699427339
				],
				[
					1.6101915324636593,
					-0.32204567736465606
				],
				[
					1.6101915324636593,
					0
				],
				[
					1.6101915324636593,
					0.3220333925781347
				],
				[
					1.6101915324636593,
					0.4830500888671736
				],
				[
					1.6101915324636593,
					0.9661124625208686
				],
				[
					1.6101915324636593,
					1.1271291588099643
				],
				[
					1.6101915324636593,
					1.6101915324636025
				],
				[
					1.6101915324636593,
					2.093241621330833
				],
				[
					1.6101915324636593,
					2.415287298695432
				],
				[
					1.6101915324636593,
					2.737320691273567
				],
				[
					1.6101915324636593,
					3.220383064927262
				],
				[
					1.6101915324636593,
					3.5424164575053965
				],
				[
					1.6101915324636593,
					3.7034331537944922
				],
				[
					1.6101915324636593,
					4.025478831159091
				],
				[
					1.6101915324636593,
					4.18649552744813
				],
				[
					1.6101915324636593,
					4.347512223737226
				],
				[
					1.6101915324636593,
					4.669545616315361
				],
				[
					1.6101915324636593,
					4.830574597390921
				],
				[
					1.6101915324636593,
					5.152607989969056
				],
				[
					1.6101915324636593,
					5.313624686258095
				],
				[
					1.6101915324636593,
					5.4746413825471905
				],
				[
					1.4491748361745067,
					5.4746413825471905
				],
				[
					1.4491748361745067,
					5.313624686258095
				],
				[
					1.4491748361745067,
					5.313624686258095
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 171,
			"versionNonce": 1919906355,
			"isDeleted": false,
			"id": "_QeLYkjR9_2xq0Xp8Yag8",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 635.535456085673,
			"y": 474.8820640850727,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 5.1526202747554635,
			"height": 16.423948717214557,
			"seed": 4650792,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.16101669628909576
				],
				[
					-0.1610289810755603,
					-0.483062373653695
				],
				[
					-0.1610289810755603,
					-0.6440790699427907
				],
				[
					-0.3220456773645992,
					-0.6440790699427907
				],
				[
					-0.3220456773645992,
					-0.9661124625209254
				],
				[
					-0.3220456773645992,
					-1.1271291588099643
				],
				[
					-0.3220456773645992,
					-1.2881581398855246
				],
				[
					-0.3220456773645992,
					-1.6101915324636593
				],
				[
					-0.3220456773645992,
					-1.771208228752755
				],
				[
					-0.644079069942677,
					-2.0932539061173543
				],
				[
					-0.644079069942677,
					-2.254270602406393
				],
				[
					-0.8050957662318297,
					-2.7373206912736237
				],
				[
					-0.8050957662318297,
					-2.898349672349184
				],
				[
					-1.1271414435964289,
					-3.7034454385810136
				],
				[
					-1.2881581398854678,
					-4.025478831159091
				],
				[
					-1.2881581398854678,
					-4.508541204812786
				],
				[
					-1.2881581398854678,
					-4.991591293680017
				],
				[
					-1.2881581398854678,
					-5.313636971044616
				],
				[
					-1.2881581398854678,
					-5.635670363622751
				],
				[
					-1.6101915324636593,
					-6.44076612985458
				],
				[
					-1.771220513539106,
					-6.762799522432715
				],
				[
					-1.771220513539106,
					-7.24586189608641
				],
				[
					-1.771220513539106,
					-7.728924269740048
				],
				[
					-1.9322372098282585,
					-8.211974358607279
				],
				[
					-1.9322372098282585,
					-8.372991054896374
				],
				[
					-2.2542706024063364,
					-8.85605342855007
				],
				[
					-2.2542706024063364,
					-9.178086821128147
				],
				[
					-2.2542706024063364,
					-9.339115802203708
				],
				[
					-2.2542706024063364,
					-9.661149194781842
				],
				[
					-2.415287298695489,
					-9.822165891070938
				],
				[
					-2.415287298695489,
					-9.983182587359977
				],
				[
					-2.415287298695489,
					-10.305228264724576
				],
				[
					-2.415287298695489,
					-10.466244961013672
				],
				[
					-2.415287298695489,
					-10.788278353591807
				],
				[
					-2.415287298695489,
					-10.949307334667367
				],
				[
					-2.415287298695489,
					-11.271340727245502
				],
				[
					-2.415287298695489,
					-11.432357423534597
				],
				[
					-2.737332976060088,
					-11.593374119823636
				],
				[
					-2.898349672349127,
					-11.915419797188235
				],
				[
					-2.898349672349127,
					-12.076436493477331
				],
				[
					-3.220383064927205,
					-12.076436493477331
				],
				[
					-3.220383064927205,
					-12.398469886055466
				],
				[
					-3.3814120460027652,
					-12.398469886055466
				],
				[
					-3.3814120460027652,
					-12.559498867131026
				],
				[
					-3.542428742291918,
					-12.720515563420065
				],
				[
					-3.542428742291918,
					-13.0425489559982
				],
				[
					-3.8644621348699957,
					-13.203565652287296
				],
				[
					-4.025478831159035,
					-13.686628025940934
				],
				[
					-4.025478831159035,
					-14.008661418519125
				],
				[
					-4.347524508523634,
					-14.169690399594629
				],
				[
					-4.508541204812786,
					-14.330707095883724
				],
				[
					-4.508541204812786,
					-14.813757184750898
				],
				[
					-4.830574597390864,
					-15.135802862115554
				],
				[
					-4.830574597390864,
					-15.296819558404593
				],
				[
					-4.830574597390864,
					-15.618852950982728
				],
				[
					-4.9916035784664246,
					-15.618852950982728
				],
				[
					-4.9916035784664246,
					-15.779881932058288
				],
				[
					-4.9916035784664246,
					-15.940898628347327
				],
				[
					-5.1526202747554635,
					-16.26293202092546
				],
				[
					-5.1526202747554635,
					-16.423948717214557
				],
				[
					-5.1526202747554635,
					-16.101915324636423
				],
				[
					-5.1526202747554635,
					-15.940898628347327
				],
				[
					-5.1526202747554635,
					-15.940898628347327
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 164,
			"versionNonce": 1142832765,
			"isDeleted": false,
			"id": "DkxY4-F3GTitZrqSGjRzb",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 630.3828358109175,
			"y": 459.10218215301444,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 6.118720452490038,
			"height": 4.347512223737283,
			"seed": 1031311912,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158214,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.16101669628903892
				],
				[
					-0.3220333925781915,
					-0.16101669628903892
				],
				[
					-0.48305008886723044,
					-0.16101669628903892
				],
				[
					-0.48305008886723044,
					0
				],
				[
					-0.9661124625209823,
					0.32204567736465606
				],
				[
					-0.9661124625209823,
					0.483062373653695
				],
				[
					-1.1271291588100212,
					0.8050957662318297
				],
				[
					-1.4491748361746204,
					0.96612474730739
				],
				[
					-1.9322249250418508,
					1.2881581398855246
				],
				[
					-2.0932416213308898,
					1.4491748361745636
				],
				[
					-2.415287298695489,
					1.9322372098282585
				],
				[
					-2.415287298695489,
					2.0932539061173543
				],
				[
					-2.576303994984528,
					2.0932539061173543
				],
				[
					-2.576303994984528,
					2.415287298695489
				],
				[
					-2.7373206912736805,
					2.5763162797709924
				],
				[
					-2.7373206912736805,
					2.898349672349184
				],
				[
					-2.7373206912736805,
					2.737332976060088
				],
				[
					-2.7373206912736805,
					2.5763162797709924
				],
				[
					-2.7373206912736805,
					2.254270602406393
				],
				[
					-2.7373206912736805,
					2.0932539061173543
				],
				[
					-2.7373206912736805,
					1.7712205135391628
				],
				[
					-2.576303994984528,
					1.4491748361745636
				],
				[
					-2.576303994984528,
					1.1271414435964289
				],
				[
					-2.25427060240645,
					0.96612474730739
				],
				[
					-2.0932416213308898,
					0.483062373653695
				],
				[
					-1.7712082287526982,
					0.1610289810755603
				],
				[
					-1.7712082287526982,
					0
				],
				[
					-1.7712082287526982,
					-0.16101669628903892
				],
				[
					-1.6101915324636593,
					-0.4830500888671736
				],
				[
					-1.28814585509906,
					-0.4830500888671736
				],
				[
					-1.1271291588100212,
					-0.6440667851562694
				],
				[
					-1.1271291588100212,
					-0.9661124625208686
				],
				[
					-0.9661124625209823,
					-0.9661124625208686
				],
				[
					-0.9661124625209823,
					-1.1271291588099643
				],
				[
					-0.6440790699427907,
					-1.1271291588099643
				],
				[
					-0.48305008886723044,
					-1.1271291588099643
				],
				[
					-0.48305008886723044,
					-1.449162551388099
				],
				[
					-0.1610166962891526,
					-1.449162551388099
				],
				[
					0,
					-1.449162551388099
				],
				[
					0.16101669628903892,
					-1.2881458550990033
				],
				[
					0.48306237365363813,
					-1.1271291588099643
				],
				[
					0.644079069942677,
					-1.1271291588099643
				],
				[
					0.9661124625208686,
					-0.8050957662317728
				],
				[
					1.1271414435964289,
					-0.8050957662317728
				],
				[
					1.1271414435964289,
					-0.6440667851562694
				],
				[
					1.4491748361745067,
					-0.6440667851562694
				],
				[
					1.6101915324635456,
					-0.3220333925781347
				],
				[
					1.7712082287526982,
					-0.16101669628903892
				],
				[
					2.0932539061172974,
					-0.16101669628903892
				],
				[
					2.2542706024063364,
					0
				],
				[
					2.576303994984528,
					0
				],
				[
					2.7373329760599745,
					0
				],
				[
					3.059366368638166,
					0
				],
				[
					3.220383064927205,
					0
				],
				[
					3.3813997612163575,
					0
				],
				[
					3.3813997612163575,
					0
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 167,
			"versionNonce": 1120449491,
			"isDeleted": false,
			"id": "LBfD3fa1f5kqIamdec1xo",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 712.9856663402168,
			"y": 449.23975901667467,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 13.364594633362799,
			"height": 15.940886343560862,
			"seed": 76779560,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.16101669628909576
				],
				[
					0,
					-0.3220333925781347
				],
				[
					-0.3220333925781915,
					-0.6440667851562694
				],
				[
					-0.48306237365363813,
					-0.6440667851562694
				],
				[
					-0.6440667851562694,
					-0.8050957662318297
				],
				[
					-0.96612474730739,
					-0.8050957662318297
				],
				[
					-0.96612474730739,
					-1.1271291588099643
				],
				[
					-1.449162551388099,
					-1.2881458550990033
				],
				[
					-1.6101915324636593,
					-1.449162551388099
				],
				[
					-2.0932539061172974,
					-1.7712082287526982
				],
				[
					-2.5763162797710493,
					-1.932224925041794
				],
				[
					-3.0593540838517583,
					-2.415287298695432
				],
				[
					-3.5424164575053965,
					-2.7373206912736237
				],
				[
					-3.864449850083588,
					-3.0593540838517583
				],
				[
					-4.186507812234595,
					-3.3813997612163575
				],
				[
					-4.669545616315418,
					-3.864449850083531
				],
				[
					-5.152607989969056,
					-4.025478831159091
				],
				[
					-5.313636971044616,
					-4.347512223737226
				],
				[
					-5.474641382547247,
					-4.508528920026322
				],
				[
					-5.796699344698254,
					-4.669545616315361
				],
				[
					-5.957703756200885,
					-4.99159129367996
				],
				[
					-5.957703756200885,
					-5.152607989969056
				],
				[
					-6.279737148779077,
					-5.4746413825471905
				],
				[
					-6.440766129854637,
					-5.635670363622751
				],
				[
					-6.601795110930084,
					-6.118720452489981
				],
				[
					-6.923828503508275,
					-6.27973714877902
				],
				[
					-7.084832915010793,
					-6.601782826143619
				],
				[
					-7.4068908771619135,
					-6.762799522432715
				],
				[
					-7.567895288664545,
					-7.08483291501085
				],
				[
					-7.567895288664545,
					-7.24586189608641
				],
				[
					-7.889928681242736,
					-7.728911984953584
				],
				[
					-8.050957662318183,
					-7.889928681242679
				],
				[
					-8.211986643393743,
					-8.211974358607279
				],
				[
					-8.534020035971935,
					-8.372991054896318
				],
				[
					-8.695024447474452,
					-8.856053428550013
				],
				[
					-9.178086821128204,
					-9.017070124839108
				],
				[
					-9.500120213706282,
					-9.500120213706282
				],
				[
					-9.661149194781842,
					-9.983182587359977
				],
				[
					-9.822178175857402,
					-10.62726165730271
				],
				[
					-10.305215979938112,
					-11.110311746169941
				],
				[
					-10.78827835359175,
					-11.43235742353454
				],
				[
					-10.78827835359175,
					-11.593374119823636
				],
				[
					-11.271340727245502,
					-12.23745318976637
				],
				[
					-11.432369708321062,
					-12.559486582344505
				],
				[
					-11.75440310089914,
					-13.0425489559982
				],
				[
					-11.91540751240177,
					-13.203565652287239
				],
				[
					-12.237465474552891,
					-13.364582348576334
				],
				[
					-12.237465474552891,
					-13.686628025940934
				],
				[
					-12.398469886055409,
					-13.847644722229973
				],
				[
					-12.55949886713097,
					-14.169678114808164
				],
				[
					-12.55949886713097,
					-14.330694811097203
				],
				[
					-12.88153225970916,
					-14.652740488461802
				],
				[
					-13.042561240784607,
					-14.813757184750898
				],
				[
					-13.042561240784607,
					-14.974773881039994
				],
				[
					-13.364594633362799,
					-15.296819558404593
				],
				[
					-13.364594633362799,
					-15.457836254693632
				],
				[
					-13.364594633362799,
					-15.779869647271767
				],
				[
					-13.364594633362799,
					-15.940886343560862
				],
				[
					-13.364594633362799,
					-15.940886343560862
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 147,
			"versionNonce": 841705181,
			"isDeleted": false,
			"id": "G2DBKqvb7YZrlypn_IWQ2",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 691.2480806519576,
			"y": 427.1801399358374,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 2.5763162797710493,
			"height": 8.372997197289578,
			"seed": 1125611304,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.32203953497139537
				],
				[
					0.3220333925781915,
					-0.48305623126049113
				],
				[
					0.4830623736537518,
					-0.48305623126049113
				],
				[
					0.4830623736537518,
					-0.8050957662318297
				],
				[
					0.6440667851562694,
					-0.9661186049141293
				],
				[
					0.96612474730739,
					-1.288151997492264
				],
				[
					0.96612474730739,
					-1.4491748361745636
				],
				[
					1.1271291588100212,
					-1.6101915324636593
				],
				[
					1.1271291588100212,
					-1.9322310674350547
				],
				[
					1.1271291588100212,
					-2.0932477637240936
				],
				[
					1.449162551388099,
					-2.415287298695489
				],
				[
					1.449162551388099,
					-2.8983435299559233
				],
				[
					1.449162551388099,
					-3.059366368638223
				],
				[
					1.449162551388099,
					-3.2203830649273186
				],
				[
					1.449162551388099,
					-3.542422599898657
				],
				[
					1.449162551388099,
					-3.3814059036096182
				],
				[
					1.449162551388099,
					-3.2203830649273186
				],
				[
					1.6101915324636593,
					-3.059366368638223
				],
				[
					1.6101915324636593,
					-2.7373268336668275
				],
				[
					1.6101915324636593,
					-2.254270602406393
				],
				[
					1.6101915324636593,
					-2.0932477637240936
				],
				[
					1.6101915324636593,
					-1.6101915324636593
				],
				[
					1.6101915324636593,
					-1.4491748361745636
				],
				[
					1.6101915324636593,
					-0.9661186049141293
				],
				[
					1.6101915324636593,
					-0.1610228386822996
				],
				[
					1.6101915324636593,
					0.16101669628903892
				],
				[
					1.6101915324636593,
					0.9661124625208686
				],
				[
					1.6101915324636593,
					1.288151997492264
				],
				[
					1.6101915324636593,
					1.7712082287526982
				],
				[
					1.7712205135392196,
					2.576303994984528
				],
				[
					1.7712205135392196,
					2.898349672349127
				],
				[
					2.093253906117411,
					3.3813997612163007
				],
				[
					2.093253906117411,
					3.7034454385809568
				],
				[
					2.2542583176199287,
					3.8644621348699957
				],
				[
					2.2542583176199287,
					4.18649552744813
				],
				[
					2.2542583176199287,
					4.347512223737226
				],
				[
					2.5763162797710493,
					4.347512223737226
				],
				[
					2.5763162797710493,
					4.50854120481273
				],
				[
					2.5763162797710493,
					4.830574597390921
				],
				[
					2.5763162797710493,
					4.830574597390921
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 135,
			"versionNonce": 1707655539,
			"isDeleted": false,
			"id": "4MgkQBWf__glovzeq4Rix",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 689.1548267458403,
			"y": 419.4512218084906,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 4.669557901101825,
			"height": 12.55949886713097,
			"seed": 382567720,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.1610228386822996
				],
				[
					0,
					-0.32203953497139537
				],
				[
					0,
					-0.6440790699427339
				],
				[
					0,
					-0.8050957662318297
				],
				[
					-0.3220333925781915,
					-0.8050957662318297
				],
				[
					-0.3220333925781915,
					-1.127135301203225
				],
				[
					-0.6440667851562694,
					-1.771214371145959
				],
				[
					-0.9661001777343472,
					-2.415287298695489
				],
				[
					-1.1271291588099075,
					-2.898349672349127
				],
				[
					-1.6101915324636593,
					-3.3814059036095614
				],
				[
					-1.9322249250417372,
					-4.025478831159091
				],
				[
					-2.2542583176199287,
					-4.669557901101825
				],
				[
					-2.737320691273567,
					-5.635670363622751
				],
				[
					-3.220383064927205,
					-6.60178896853688
				],
				[
					-3.5424164575053965,
					-7.40688473476871
				],
				[
					-3.7034331537944354,
					-8.050957662318183
				],
				[
					-3.8644621348699957,
					-8.695036732260974
				],
				[
					-4.186495527448187,
					-9.339115802203708
				],
				[
					-4.186495527448187,
					-10.14421156843548
				],
				[
					-4.186495527448187,
					-10.305228264724576
				],
				[
					-4.347512223737226,
					-10.78828449598501
				],
				[
					-4.347512223737226,
					-11.271340727245502
				],
				[
					-4.347512223737226,
					-11.75440310089914
				],
				[
					-4.347512223737226,
					-11.915419797188235
				],
				[
					-4.669557901101825,
					-12.076436493477274
				],
				[
					-4.669557901101825,
					-12.39847602844867
				],
				[
					-4.669557901101825,
					-12.55949886713097
				],
				[
					-4.669557901101825,
					-12.55949886713097
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 160,
			"versionNonce": 1228178237,
			"isDeleted": false,
			"id": "S0dFyOx9yURB836k_c60l",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 683.8412020595822,
			"y": 406.8917229413596,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 6.279737148779077,
			"height": 3.220383064927262,
			"seed": 531795752,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.3220333925781347
				],
				[
					0,
					-0.16101669628903892
				],
				[
					-0.1610289810755603,
					-0.16101669628903892
				],
				[
					-0.48306237365363813,
					0
				],
				[
					-0.6440790699427907,
					0.32203953497139537
				],
				[
					-0.96612474730739,
					0.483062373653695
				],
				[
					-1.1271414435964289,
					0.6440790699427339
				],
				[
					-1.4491748361746204,
					1.127135301203225
				],
				[
					-1.6101915324636593,
					1.127135301203225
				],
				[
					-1.7712205135392196,
					1.4491748361745636
				],
				[
					-1.7712205135392196,
					1.6101915324636593
				],
				[
					-2.0932539061172974,
					1.6101915324636593
				],
				[
					-2.0932539061172974,
					1.9322310674349978
				],
				[
					-2.25427060240645,
					2.0932539061172974
				],
				[
					-2.25427060240645,
					2.254270602406393
				],
				[
					-2.25427060240645,
					2.0932539061172974
				],
				[
					-1.9322372098282585,
					1.771214371145959
				],
				[
					-1.9322372098282585,
					1.6101915324636593
				],
				[
					-1.7712205135392196,
					1.2881581398854678
				],
				[
					-1.6101915324636593,
					1.127135301203225
				],
				[
					-1.6101915324636593,
					0.8050957662318297
				],
				[
					-1.2881581398855815,
					0.6440790699427339
				],
				[
					-1.1271414435964289,
					0.483062373653695
				],
				[
					-1.1271414435964289,
					0.1610228386822996
				],
				[
					-0.8050957662318297,
					0
				],
				[
					-0.6440790699427907,
					0
				],
				[
					-0.6440790699427907,
					-0.3220333925781347
				],
				[
					-0.3220456773645992,
					-0.4830562312604343
				],
				[
					-0.1610289810755603,
					-0.4830562312604343
				],
				[
					-0.1610289810755603,
					-0.8050957662318297
				],
				[
					0,
					-0.8050957662318297
				],
				[
					0,
					-0.9661124625208686
				],
				[
					0.32203339257807784,
					-0.9661124625208686
				],
				[
					0.48305008886723044,
					-0.9661124625208686
				],
				[
					0.8050957662318297,
					-0.9661124625208686
				],
				[
					0.9661124625208686,
					-0.64407292754953
				],
				[
					1.2881458550989464,
					-0.4830562312604343
				],
				[
					1.449162551388099,
					-0.4830562312604343
				],
				[
					1.6101915324636593,
					-0.4830562312604343
				],
				[
					1.6101915324636593,
					-0.16101669628903892
				],
				[
					1.9322249250417372,
					-0.16101669628903892
				],
				[
					2.0932416213308898,
					0
				],
				[
					2.4152750139089676,
					0
				],
				[
					2.576303994984528,
					0.32203953497139537
				],
				[
					2.8983373875626057,
					0.32203953497139537
				],
				[
					3.059366368638166,
					0.483062373653695
				],
				[
					3.2203707801407973,
					0.483062373653695
				],
				[
					3.542428742291804,
					0.483062373653695
				],
				[
					3.542428742291804,
					0.6440790699427339
				],
				[
					3.7034331537944354,
					0.6440790699427339
				],
				[
					3.7034331537944354,
					0.9661186049141293
				],
				[
					4.025466546372627,
					0.9661186049141293
				],
				[
					4.025466546372627,
					0.9661186049141293
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 138,
			"versionNonce": 1958091539,
			"isDeleted": false,
			"id": "2CBohAgnvcK5l1DVkIXGX",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 713.303490835125,
			"y": 489.2507027392011,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 4.343719199519569,
			"height": 9.230372230396824,
			"seed": 876002344,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.27147727187292503
				],
				[
					0,
					-0.8144525280069956
				],
				[
					0,
					-1.0859297998798638
				],
				[
					0,
					-1.3574070717528457
				],
				[
					0.2714979842611456,
					-1.9003616154986958
				],
				[
					0.8144525280069956,
					-2.1718595997597845
				],
				[
					1.0859297998798638,
					-2.1718595997597845
				],
				[
					1.6289050560139913,
					-2.7148141435056345
				],
				[
					1.6289050560139913,
					-2.9862914153785596
				],
				[
					1.6289050560139913,
					-3.5292666715125733
				],
				[
					1.9003823278868595,
					-3.800743943385555
				],
				[
					2.4433368716327095,
					-3.800743943385555
				],
				[
					2.7148141435056914,
					-4.072221215258423
				],
				[
					2.7148141435056914,
					-4.6151757590042735
				],
				[
					2.7148141435056914,
					-4.886673743265419
				],
				[
					2.7148141435056914,
					-5.429628287011269
				],
				[
					2.986312127766837,
					-5.429628287011269
				],
				[
					2.986312127766837,
					-5.701105558884194
				],
				[
					3.5292666715125733,
					-5.701105558884194
				],
				[
					3.5292666715125733,
					-6.244080815018265
				],
				[
					3.800743943385555,
					-6.244080815018265
				],
				[
					3.800743943385555,
					-6.515558086891133
				],
				[
					3.800743943385555,
					-6.787035358764115
				],
				[
					3.800743943385555,
					-7.329989902509965
				],
				[
					3.800743943385555,
					-7.601487886771054
				],
				[
					4.343719199519569,
					-7.601487886771054
				],
				[
					4.343719199519569,
					-8.144442430516904
				],
				[
					4.343719199519569,
					-8.415919702389829
				],
				[
					4.343719199519569,
					-8.958894958523842
				],
				[
					4.343719199519569,
					-9.230372230396824
				],
				[
					4.343719199519569,
					-9.230372230396824
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 172,
			"versionNonce": 1838879645,
			"isDeleted": false,
			"id": "bt-R8IIFGy59DNl6Rk31_",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 717.5987861014828,
			"y": 469.09359324299305,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 4.266679885906797,
			"height": 6.914967049541417,
			"seed": 567638104,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.1471245702273336,
					0
				],
				[
					0.44138493556749836,
					0
				],
				[
					0.5885095057949457,
					0
				],
				[
					0.8827586462497266,
					0
				],
				[
					0.8827586462497266,
					-0.2942491404548946
				],
				[
					1.0298944413623303,
					-0.2942491404548946
				],
				[
					1.0298944413623303,
					-0.44137371068228504
				],
				[
					1.1770190115897776,
					-0.44137371068228504
				],
				[
					1.4712681520446722,
					-0.44137371068228504
				],
				[
					1.4712681520446722,
					-0.735634076022393
				],
				[
					1.6183927222721195,
					-0.735634076022393
				],
				[
					1.6183927222721195,
					-0.8827586462498402
				],
				[
					1.9126530876121706,
					-0.8827586462498402
				],
				[
					2.059777657839618,
					-0.8827586462498402
				],
				[
					2.3540267982945124,
					-0.8827586462498402
				],
				[
					2.3540267982945124,
					-0.5884982809097323
				],
				[
					2.3540267982945124,
					0
				],
				[
					2.3540267982945124,
					0.14713579511260377
				],
				[
					2.3540267982945124,
					0.44138493556749836
				],
				[
					2.206902228067065,
					0.44138493556749836
				],
				[
					2.206902228067065,
					0.5885095057949457
				],
				[
					2.206902228067065,
					1.029894441362444
				],
				[
					2.059777657839618,
					1.471268152044729
				],
				[
					2.059777657839618,
					1.6184039471573897
				],
				[
					2.059777657839618,
					2.0597776578396747
				],
				[
					2.059777657839618,
					2.3540380231797258
				],
				[
					2.059777657839618,
					2.501162593407173
				],
				[
					2.059777657839618,
					2.942536304089458
				],
				[
					2.059777657839618,
					3.0896720992021187
				],
				[
					2.059777657839618,
					3.3839212396569565
				],
				[
					2.059777657839618,
					3.5310458098844038
				],
				[
					2.059777657839618,
					3.825306175224455
				],
				[
					2.059777657839618,
					3.972430745451902
				],
				[
					2.059777657839618,
					4.413804456134244
				],
				[
					2.059777657839618,
					4.560940251246848
				],
				[
					2.059777657839618,
					4.855189391701742
				],
				[
					2.059777657839618,
					5.002313961929133
				],
				[
					2.059777657839618,
					5.14943853215658
				],
				[
					2.059777657839618,
					5.443698897496631
				],
				[
					1.7655285173847233,
					5.443698897496631
				],
				[
					1.7655285173847233,
					5.5908234677240785
				],
				[
					1.6183927222721195,
					5.5908234677240785
				],
				[
					1.324143581817225,
					5.5908234677240785
				],
				[
					1.1770190115897776,
					5.885072608178973
				],
				[
					1.0298944413623303,
					5.885072608178973
				],
				[
					0.7356340760222793,
					5.885072608178973
				],
				[
					0.5885095057949457,
					5.885072608178973
				],
				[
					0.29426036534005107,
					5.885072608178973
				],
				[
					0.1471245702273336,
					5.885072608178973
				],
				[
					0,
					5.885072608178973
				],
				[
					-0.2942491404548946,
					5.885072608178973
				],
				[
					-0.4413737106823419,
					5.885072608178973
				],
				[
					-0.735634076022393,
					5.885072608178973
				],
				[
					-0.5885095057949457,
					5.885072608178973
				],
				[
					-0.4413737106823419,
					5.885072608178973
				],
				[
					-0.1471245702274473,
					5.885072608178973
				],
				[
					-0.1471245702274473,
					6.032208403291577
				],
				[
					0,
					6.032208403291577
				],
				[
					0.1471245702273336,
					6.032208403291577
				],
				[
					0.44138493556749836,
					6.032208403291577
				],
				[
					0.5885095057949457,
					6.032208403291577
				],
				[
					1.0298944413623303,
					6.032208403291577
				],
				[
					1.1770190115897776,
					6.032208403291577
				],
				[
					1.4712681520446722,
					6.032208403291577
				],
				[
					1.6183927222721195,
					6.032208403291577
				],
				[
					1.9126530876121706,
					6.032208403291577
				],
				[
					2.059777657839618,
					6.032208403291577
				],
				[
					2.3540267982945124,
					6.032208403291577
				],
				[
					2.6482871636345635,
					6.032208403291577
				],
				[
					2.942536304089458,
					6.032208403291577
				],
				[
					3.0896608743169054,
					6.032208403291577
				],
				[
					3.3839212396569565,
					6.032208403291577
				],
				[
					3.5310458098844038,
					6.032208403291577
				],
				[
					3.5310458098844038,
					6.032208403291577
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 139,
			"versionNonce": 470237363,
			"isDeleted": false,
			"id": "Jws9i1w3tRyN86CKxHgVE",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 723.0424849989794,
			"y": 467.7694608860609,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 6.914955824656204,
			"height": 8.091974836246038,
			"seed": 62387288,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.14713579511260377
				],
				[
					0.1471245702274473,
					-0.14713579511260377
				],
				[
					0.1471245702274473,
					-0.44138493556749836
				],
				[
					0.4413737106823419,
					-0.44138493556749836
				],
				[
					0.4413737106823419,
					-0.5885095057948888
				],
				[
					0.5884982809097892,
					-0.8827698711349967
				],
				[
					1.0298832164772875,
					-1.0298944413623872
				],
				[
					1.1770077867047348,
					-1.3241435818172818
				],
				[
					1.471268152044786,
					-1.471268152044729
				],
				[
					1.6183927222722332,
					-1.6184039471573328
				],
				[
					1.9126418627271278,
					-2.0597776578396747
				],
				[
					2.0597664329544614,
					-2.3540380231797258
				],
				[
					2.3540267982945124,
					-2.795411733862011
				],
				[
					2.5011513685219597,
					-2.942536304089458
				],
				[
					2.648275938749407,
					-3.0896720992021187
				],
				[
					2.942536304089458,
					-3.5310458098844038
				],
				[
					3.0896608743169054,
					-3.825306175224455
				],
				[
					3.3839100147718,
					-3.972430745451902
				],
				[
					3.5310345849992473,
					-4.413804456134187
				],
				[
					3.8252949503392983,
					-4.560940251246848
				],
				[
					3.8252949503392983,
					-4.8551893917016855
				],
				[
					3.9724195205667456,
					-5.002313961929133
				],
				[
					4.119544090794193,
					-5.296574327269184
				],
				[
					4.413804456134244,
					-5.443698897496631
				],
				[
					4.560929026361691,
					-5.5908234677240785
				],
				[
					4.855178166816586,
					-5.885072608178973
				],
				[
					5.002302737044033,
					-6.032208403291577
				],
				[
					5.149438532156637,
					-6.326457543746471
				],
				[
					5.4436876726115315,
					-6.326457543746471
				],
				[
					5.4436876726115315,
					-6.473582113973862
				],
				[
					5.590812242838979,
					-6.76784247931397
				],
				[
					5.88507260817903,
					-6.91496704954136
				],
				[
					6.0321971784063635,
					-7.0620916197688075
				],
				[
					6.326446318861258,
					-7.503476555336306
				],
				[
					6.473570889088705,
					-7.503476555336306
				],
				[
					6.473570889088705,
					-7.797725695791144
				],
				[
					6.620706684201309,
					-7.797725695791144
				],
				[
					6.620706684201309,
					-7.944850266018591
				],
				[
					6.914955824656204,
					-7.944850266018591
				],
				[
					6.914955824656204,
					-8.091974836246038
				],
				[
					6.914955824656204,
					-8.091974836246038
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 132,
			"versionNonce": 2073073661,
			"isDeleted": false,
			"id": "YJDmevXJcn84jEoabhuSh",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 727.1620290897736,
			"y": 457.47058382174777,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 5.885072608178916,
			"height": 3.2367854445443527,
			"seed": 716766040,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.29426036534005107,
					0
				],
				[
					0.44138493556749836,
					0
				],
				[
					0.735634076022393,
					0
				],
				[
					0.8827586462498402,
					0
				],
				[
					1.3241435818173386,
					0.1471245702274473
				],
				[
					1.471268152044786,
					0.1471245702274473
				],
				[
					2.206902228067065,
					0.1471245702274473
				],
				[
					2.3540267982945124,
					0.2942491404548946
				],
				[
					2.942536304089458,
					0.2942491404548946
				],
				[
					3.3839212396569565,
					0.2942491404548946
				],
				[
					3.8252949503392983,
					0.2942491404548946
				],
				[
					4.413804456134244,
					0.2942491404548946
				],
				[
					4.855189391701742,
					0.2942491404548946
				],
				[
					5.149438532156637,
					0.2942491404548946
				],
				[
					5.2965631023839705,
					0.2942491404548946
				],
				[
					5.443698897496688,
					0.2942491404548946
				],
				[
					5.737948037951469,
					0.2942491404548946
				],
				[
					5.885072608178916,
					0.2942491404548946
				],
				[
					5.885072608178916,
					0.5884982809097323
				],
				[
					5.885072608178916,
					0.735634076022393
				],
				[
					5.885072608178916,
					0.8827586462497834
				],
				[
					5.590823467724022,
					1.177007786704678
				],
				[
					5.590823467724022,
					1.3241323569321253
				],
				[
					5.443698897496688,
					1.3241323569321253
				],
				[
					5.443698897496688,
					1.6183927222721763
				],
				[
					5.2965631023839705,
					2.0597664329545182
				],
				[
					5.2965631023839705,
					2.206902228067122
				],
				[
					5.2965631023839705,
					2.3540267982945693
				],
				[
					5.002313961929076,
					2.3540267982945693
				],
				[
					5.002313961929076,
					2.648275938749407
				],
				[
					5.002313961929076,
					2.7954005089768543
				],
				[
					5.002313961929076,
					3.0896608743169054
				],
				[
					5.002313961929076,
					3.2367854445443527
				],
				[
					5.002313961929076,
					3.2367854445443527
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 139,
			"versionNonce": 895660627,
			"isDeleted": false,
			"id": "lF2MeUqogyErIVf_Tuy03",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 766.444884259414,
			"y": 489.9856077369594,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 7.356340760223702,
			"height": 9.857503353630818,
			"seed": 126431064,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.2942491404548946,
					0
				],
				[
					-0.2942491404548946,
					-0.29426036534005107
				],
				[
					-0.4413624857971854,
					-0.29426036534005107
				],
				[
					-0.5884982809097892,
					-0.44138493556749836
				],
				[
					-0.5884982809097892,
					-0.5885095057948888
				],
				[
					-1.0298832164772875,
					-0.8827586462497834
				],
				[
					-1.3241323569321821,
					-1.3241435818172818
				],
				[
					-1.471268152044786,
					-1.7655285173847801
				],
				[
					-1.9126306378418576,
					-2.059777657839618
				],
				[
					-2.059766432954575,
					-2.501162593407116
				],
				[
					-2.5011513685219597,
					-2.795411733862011
				],
				[
					-2.7954005089768543,
					-3.236796669429509
				],
				[
					-3.089649649431749,
					-3.5310458098844038
				],
				[
					-3.3838987898866435,
					-3.972430745451902
				],
				[
					-3.5310345849992473,
					-4.413804456134187
				],
				[
					-3.825283725454142,
					-4.708064821474238
				],
				[
					-3.9724195205667456,
					-5.002313961929133
				],
				[
					-4.26666866102164,
					-5.2965631023839705
				],
				[
					-4.560917801476535,
					-5.737948037951469
				],
				[
					-4.855166941931429,
					-6.0321971784063635
				],
				[
					-5.002302737044033,
					-6.326457543746415
				],
				[
					-5.296551877498814,
					-6.473582113973862
				],
				[
					-5.4436876726115315,
					-6.767831254428756
				],
				[
					-5.590801017953709,
					-6.91496704954136
				],
				[
					-5.88507260817903,
					-7.209216189996255
				],
				[
					-5.88507260817903,
					-7.356340760223645
				],
				[
					-6.032185953521207,
					-7.5034653304510925
				],
				[
					-6.326435093976102,
					-7.797725695791144
				],
				[
					-6.326435093976102,
					-7.944850266018591
				],
				[
					-6.473570889088705,
					-8.239099406473485
				],
				[
					-6.7678200295436,
					-8.38623520158609
				],
				[
					-6.7678200295436,
					-8.680484342040984
				],
				[
					-6.914955824656204,
					-8.827608912268374
				],
				[
					-6.914955824656204,
					-8.974733482495822
				],
				[
					-6.914955824656204,
					-9.268993847835873
				],
				[
					-7.0620691699984945,
					-9.268993847835873
				],
				[
					-7.0620691699984945,
					-9.41611841806332
				],
				[
					-7.0620691699984945,
					-9.710367558518215
				],
				[
					-7.0620691699984945,
					-9.857503353630818
				],
				[
					-7.356340760223702,
					-9.857503353630818
				],
				[
					-7.356340760223702,
					-9.857503353630818
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 185,
			"versionNonce": 1293324381,
			"isDeleted": false,
			"id": "BbLGxDQ6CbEB_s_o_gmZT",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 747.9069077886273,
			"y": 473.06602398844495,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 5.149449757041793,
			"height": 5.590812242838865,
			"seed": 251205208,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.29426036534005107
				],
				[
					0,
					-0.1471245702274473
				],
				[
					0,
					0
				],
				[
					0,
					0.2942491404548946
				],
				[
					0,
					0.4413737106823419
				],
				[
					0,
					0.735634076022393
				],
				[
					0,
					0.8827586462498402
				],
				[
					0,
					1.0298832164772307
				],
				[
					0,
					1.3241435818173386
				],
				[
					0,
					1.471268152044729
				],
				[
					0,
					1.7655172924996236
				],
				[
					0,
					1.912641862727071
				],
				[
					0.29426036534005107,
					2.206902228067122
				],
				[
					0.29426036534005107,
					2.3540267982945693
				],
				[
					0.44138493556749836,
					2.3540267982945693
				],
				[
					0.44138493556749836,
					2.5011513685219597
				],
				[
					0.7356453009075494,
					2.5011513685219597
				],
				[
					0.7356453009075494,
					2.7954117338620676
				],
				[
					0.8827586462498402,
					2.7954117338620676
				],
				[
					0.8827586462498402,
					2.942536304089458
				],
				[
					1.1770302364750478,
					2.942536304089458
				],
				[
					1.3241435818173386,
					2.942536304089458
				],
				[
					1.4712793769299424,
					2.942536304089458
				],
				[
					1.765528517384837,
					3.2367854445443527
				],
				[
					1.9126643124974407,
					3.2367854445443527
				],
				[
					2.2069134529523353,
					3.2367854445443527
				],
				[
					2.3540267982945124,
					3.2367854445443527
				],
				[
					2.6482983885198337,
					3.0896608743169054
				],
				[
					2.795411733862011,
					3.0896608743169054
				],
				[
					2.9425475289746146,
					2.942536304089458
				],
				[
					2.9425475289746146,
					2.648275938749407
				],
				[
					3.236796669429509,
					2.648275938749407
				],
				[
					3.3839324645422266,
					2.5011513685219597
				],
				[
					3.6781816049970075,
					2.3540267982945693
				],
				[
					3.8252949503392983,
					2.3540267982945693
				],
				[
					3.8252949503392983,
					2.0597776578396747
				],
				[
					3.972430745451902,
					1.912641862727071
				],
				[
					4.266679885906797,
					1.6183927222721763
				],
				[
					4.4138156810194005,
					1.471268152044729
				],
				[
					4.4138156810194005,
					1.177007786704678
				],
				[
					4.708064821474295,
					1.0298832164772307
				],
				[
					4.855200616586899,
					0.8827586462498402
				],
				[
					4.855200616586899,
					0.5885095057949457
				],
				[
					5.149449757041793,
					0.4413737106823419
				],
				[
					5.149449757041793,
					0.1471245702274473
				],
				[
					5.149449757041793,
					0
				],
				[
					5.149449757041793,
					-0.29426036534005107
				],
				[
					5.149449757041793,
					-0.44138493556749836
				],
				[
					5.149449757041793,
					-0.5885095057949457
				],
				[
					5.149449757041793,
					-0.8827586462497834
				],
				[
					5.00231396192919,
					-1.029894441362444
				],
				[
					5.00231396192919,
					-1.3241435818172818
				],
				[
					4.855200616586899,
					-1.3241435818172818
				],
				[
					4.855200616586899,
					-1.471268152044729
				],
				[
					4.560929026361691,
					-1.471268152044729
				],
				[
					4.560929026361691,
					-1.6183927222721763
				],
				[
					4.4138156810194005,
					-1.6183927222721763
				],
				[
					4.119566540564506,
					-1.9126530876122274
				],
				[
					3.972430745451902,
					-1.9126530876122274
				],
				[
					3.8252949503392983,
					-1.9126530876122274
				],
				[
					3.8252949503392983,
					-2.0597776578396747
				],
				[
					3.5310458098844038,
					-2.0597776578396747
				],
				[
					3.3839324645422266,
					-2.0597776578396747
				],
				[
					3.0896608743169054,
					-2.0597776578396747
				],
				[
					2.9425475289746146,
					-2.3540267982945124
				],
				[
					2.795411733862011,
					-2.3540267982945124
				],
				[
					2.50116259340723,
					-2.3540267982945124
				],
				[
					2.3540267982945124,
					-2.3540267982945124
				],
				[
					2.059777657839618,
					-2.3540267982945124
				],
				[
					1.9126643124974407,
					-2.3540267982945124
				],
				[
					1.6183927222722332,
					-2.3540267982945124
				],
				[
					1.4712793769299424,
					-2.206902228067065
				],
				[
					1.3241435818173386,
					-2.206902228067065
				],
				[
					1.029894441362444,
					-2.206902228067065
				],
				[
					1.029894441362444,
					-2.0597776578396747
				],
				[
					0.8827586462498402,
					-2.0597776578396747
				],
				[
					0.8827586462498402,
					-1.7655285173847801
				],
				[
					0.5885095057949457,
					-1.7655285173847801
				],
				[
					0.5885095057949457,
					-1.6183927222721763
				],
				[
					0.44138493556749836,
					-1.6183927222721763
				],
				[
					0.44138493556749836,
					-1.471268152044729
				],
				[
					0.14713579511260377,
					-1.471268152044729
				],
				[
					0.14713579511260377,
					-1.1770190115898913
				],
				[
					0.14713579511260377,
					-1.029894441362444
				],
				[
					0.14713579511260377,
					-0.735634076022393
				],
				[
					0.14713579511260377,
					-0.5885095057949457
				],
				[
					0.14713579511260377,
					-0.5885095057949457
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 122,
			"versionNonce": 564064243,
			"isDeleted": false,
			"id": "x9z2ix8acFsMus3S4sCpo",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 747.3184095077175,
			"y": 466.5924418744711,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 0.7356340760222793,
			"height": 6.914955824656204,
			"seed": 1312637784,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.2942491404548946
				],
				[
					0,
					-0.44138493556749836
				],
				[
					0,
					-0.5885095057949457
				],
				[
					0,
					-1.0298832164772875
				],
				[
					0,
					-1.3241435818173386
				],
				[
					0,
					-1.7655172924996236
				],
				[
					0,
					-1.9126530876122843
				],
				[
					0,
					-2.3540267982945693
				],
				[
					0,
					-2.942536304089515
				],
				[
					0,
					-3.3839212396570133
				],
				[
					-0.29426036534005107,
					-3.8252949503392983
				],
				[
					-0.29426036534005107,
					-4.413804456134244
				],
				[
					-0.44138493556749836,
					-4.855189391701742
				],
				[
					-0.44138493556749836,
					-5.00231396192919
				],
				[
					-0.44138493556749836,
					-5.443687672611475
				],
				[
					-0.44138493556749836,
					-5.737948037951526
				],
				[
					-0.44138493556749836,
					-5.885072608178973
				],
				[
					-0.7356340760222793,
					-5.885072608178973
				],
				[
					-0.7356340760222793,
					-6.03219717840642
				],
				[
					-0.7356340760222793,
					-6.326457543746471
				],
				[
					-0.7356340760222793,
					-6.473582113973919
				],
				[
					-0.7356340760222793,
					-6.767831254428756
				],
				[
					-0.7356340760222793,
					-6.914955824656204
				],
				[
					-0.7356340760222793,
					-6.914955824656204
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 136,
			"versionNonce": 2147384509,
			"isDeleted": false,
			"id": "CkApnn990PlUqM75--IL7",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 745.2586318498779,
			"y": 458.0590821026575,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 4.266679885906797,
			"height": 2.3540380231797258,
			"seed": 1462748504,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.29426036534005107,
					0.14713579511266062
				],
				[
					-0.29426036534005107,
					0.44138493556749836
				],
				[
					-0.44138493556749836,
					0.44138493556749836
				],
				[
					-0.44138493556749836,
					0.5885095057949457
				],
				[
					-0.735634076022393,
					1.029894441362444
				],
				[
					-0.8827586462498402,
					1.029894441362444
				],
				[
					-0.8827586462498402,
					1.1770190115898913
				],
				[
					-1.1770190115898913,
					1.1770190115898913
				],
				[
					-1.1770190115898913,
					1.471268152044786
				],
				[
					-1.1770190115898913,
					1.6184039471573897
				],
				[
					-1.029894441362444,
					1.6184039471573897
				],
				[
					-0.8827586462498402,
					1.3241435818173386
				],
				[
					-0.5885095057949457,
					1.1770190115898913
				],
				[
					-0.44138493556749836,
					1.029894441362444
				],
				[
					-0.1471245702274473,
					0.735634076022393
				],
				[
					0.1471245702274473,
					0.5885095057949457
				],
				[
					0.4413737106823419,
					0.29426036534005107
				],
				[
					0.4413737106823419,
					0.14713579511266062
				],
				[
					0.5885095057949457,
					0
				],
				[
					0.5885095057949457,
					-0.29424914045483774
				],
				[
					0.8827586462498402,
					-0.29424914045483774
				],
				[
					0.8827586462498402,
					-0.44137371068228504
				],
				[
					1.0298832164771738,
					-0.44137371068228504
				],
				[
					1.0298832164771738,
					-0.7356340760223361
				],
				[
					1.1770077867046211,
					-0.7356340760223361
				],
				[
					1.471268152044786,
					-0.7356340760223361
				],
				[
					1.471268152044786,
					-0.5884982809097323
				],
				[
					1.6183927222721195,
					-0.44137371068228504
				],
				[
					1.912641862727014,
					-0.1471245702274473
				],
				[
					2.059777657839618,
					0
				],
				[
					2.3540267982945124,
					0.14713579511266062
				],
				[
					2.5011513685219597,
					0.14713579511266062
				],
				[
					2.5011513685219597,
					0.44138493556749836
				],
				[
					2.648275938749407,
					0.44138493556749836
				],
				[
					2.648275938749407,
					0.5885095057949457
				],
				[
					2.942536304089458,
					0.5885095057949457
				],
				[
					3.0896608743169054,
					0.5885095057949457
				],
				[
					3.0896608743169054,
					0.5885095057949457
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 175,
			"versionNonce": 1656912275,
			"isDeleted": false,
			"id": "AJunYmx1pAI7hYGqnBEsw",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 700.0047767396518,
			"y": 395.90680965942084,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 45.766071928730184,
			"height": 23.598147461218048,
			"seed": 1854901592,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.0726263272078995,
					0
				],
				[
					1.4301684362771994,
					0
				],
				[
					2.145279933130155,
					0
				],
				[
					2.5028220421995684,
					0
				],
				[
					2.8603641512688682,
					-0.35754210906929984
				],
				[
					3.57547564812171,
					-0.7150842181385997
				],
				[
					3.9330177571911236,
					-0.7150842181385997
				],
				[
					4.648101975329723,
					-0.7150842181385997
				],
				[
					5.005644084399023,
					-1.430195714991612
				],
				[
					5.720755581251979,
					-1.430195714991612
				],
				[
					6.078297690321278,
					-1.430195714991612
				],
				[
					6.435839799390578,
					-1.7877378240609119
				],
				[
					7.150951296243534,
					-1.7877378240609119
				],
				[
					7.508493405312834,
					-2.5028220421995115
				],
				[
					8.223577623451547,
					-2.5028220421995115
				],
				[
					8.938689120304389,
					-2.5028220421995115
				],
				[
					9.653773338443102,
					-2.860391429983167
				],
				[
					10.726426944365357,
					-2.860391429983167
				],
				[
					11.083969053434657,
					-3.575475648121767
				],
				[
					12.514164768426213,
					-3.575475648121767
				],
				[
					13.586791095634112,
					-3.9330177571910667
				],
				[
					14.659444701556367,
					-3.9330177571910667
				],
				[
					15.73207102876438,
					-4.290559866260367
				],
				[
					16.804724634686636,
					-4.290559866260367
				],
				[
					17.87737824060889,
					-5.005671363113322
				],
				[
					18.95000456781679,
					-5.005671363113322
				],
				[
					19.665116064669746,
					-5.363213472182622
				],
				[
					20.737742391877646,
					-5.363213472182622
				],
				[
					22.167938106869315,
					-6.078297690321278
				],
				[
					22.883022325007914,
					-6.435867078104934
				],
				[
					23.24059171279157,
					-6.435867078104934
				],
				[
					23.95567593093017,
					-6.435867078104934
				],
				[
					24.31321803999947,
					-6.793409187174234
				],
				[
					25.385871645921725,
					-6.793409187174234
				],
				[
					25.743413754991025,
					-6.793409187174234
				],
				[
					26.458497973129624,
					-7.5084934053128904
				],
				[
					27.531151579051993,
					-7.86603551438219
				],
				[
					27.888693688121293,
					-7.86603551438219
				],
				[
					29.31888940311285,
					-8.581147011235146
				],
				[
					30.033973621251448,
					-8.581147011235146
				],
				[
					30.391543009035104,
					-8.938689120304446
				],
				[
					31.106627227173703,
					-8.938689120304446
				],
				[
					31.464169336243003,
					-9.653773338443045
				],
				[
					31.821711445312303,
					-9.653773338443045
				],
				[
					32.89436505123467,
					-10.011342726226701
				],
				[
					33.60944926937327,
					-10.368884835296
				],
				[
					34.68210287529553,
					-11.083982692791835
				],
				[
					35.39718709343413,
					-11.083982692791835
				],
				[
					36.46984069935638,
					-12.156622659356913
				],
				[
					37.18492491749498,
					-12.156622659356913
				],
				[
					38.25757852341735,
					-12.514164768426213
				],
				[
					38.61512063248665,
					-13.22926262592199
				],
				[
					38.97266274155595,
					-13.58680473499129
				],
				[
					40.045316347478206,
					-13.944360483417825
				],
				[
					40.760400565616806,
					-14.659458340913602
				],
				[
					41.11796995340046,
					-15.017000449982902
				],
				[
					42.19059628060836,
					-15.73209830747868
				],
				[
					42.54813838967766,
					-16.08964041654798
				],
				[
					43.26324988653073,
					-16.804738274043814
				],
				[
					43.62079199560003,
					-17.162280383113114
				],
				[
					44.33587621373863,
					-17.51983613153959
				],
				[
					44.33587621373863,
					-18.23493398903537
				],
				[
					44.693445601522285,
					-18.59247609810467
				],
				[
					44.693445601522285,
					-19.307573955600503
				],
				[
					45.050987710591585,
					-19.307573955600503
				],
				[
					45.050987710591585,
					-19.665116064669803
				],
				[
					45.050987710591585,
					-20.02267181309628
				],
				[
					45.766071928730184,
					-20.73775603123488
				],
				[
					45.766071928730184,
					-21.09531177966136
				],
				[
					45.766071928730184,
					-21.810409637157193
				],
				[
					45.766071928730184,
					-22.167951746226493
				],
				[
					45.766071928730184,
					-22.88304960372227
				],
				[
					45.408529819660885,
					-22.88304960372227
				],
				[
					45.050987710591585,
					-23.24059171279157
				],
				[
					44.693445601522285,
					-23.24059171279157
				],
				[
					44.693445601522285,
					-23.598147461218048
				],
				[
					44.693445601522285,
					-23.598147461218048
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 172,
			"versionNonce": 2078924061,
			"isDeleted": false,
			"id": "bWK6dGbZ6RvlXca-RAx3o",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 752.5642578555562,
			"y": 364.0850709353941,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 11.083969053434657,
			"height": 15.017000449982902,
			"seed": 1447422040,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.35754210906929984,
					-0.7150978574957776
				],
				[
					0.35754210906929984,
					-1.0726399665651343
				],
				[
					0.7150842181385997,
					-1.0726399665651343
				],
				[
					1.4301957149916689,
					-1.4301820756344341
				],
				[
					1.7877378240609687,
					-1.4301820756344341
				],
				[
					2.1452799331302685,
					-2.145279933130155
				],
				[
					2.1452799331302685,
					-2.5028356815566895
				],
				[
					3.217933539052524,
					-2.5028356815566895
				],
				[
					3.9330177571911236,
					-3.217919899695289
				],
				[
					5.005671363113379,
					-3.575475648121767
				],
				[
					5.363213472182679,
					-4.2905735056175445
				],
				[
					5.720755581251979,
					-4.2905735056175445
				],
				[
					6.435867078105048,
					-4.2905735056175445
				],
				[
					6.793409187174348,
					-4.2905735056175445
				],
				[
					7.508493405312947,
					-4.2905735056175445
				],
				[
					7.866035514382247,
					-4.2905735056175445
				],
				[
					7.866035514382247,
					-4.648115614686844
				],
				[
					8.581147011235089,
					-4.648115614686844
				],
				[
					8.938689120304502,
					-4.648115614686844
				],
				[
					8.938689120304502,
					-3.9330177571911236
				],
				[
					8.938689120304502,
					-3.575475648121767
				],
				[
					8.938689120304502,
					-2.8603777906259893
				],
				[
					8.938689120304502,
					-2.5028356815566895
				],
				[
					8.938689120304502,
					-1.787737824060855
				],
				[
					8.938689120304502,
					-1.4301820756344341
				],
				[
					8.938689120304502,
					-1.0726399665651343
				],
				[
					8.938689120304502,
					-0.35754210906929984
				],
				[
					8.938689120304502,
					0
				],
				[
					8.938689120304502,
					0.7150978574958344
				],
				[
					8.223604902165789,
					1.0726399665651343
				],
				[
					8.223604902165789,
					1.787737824060855
				],
				[
					7.866035514382247,
					1.787737824060855
				],
				[
					7.866035514382247,
					2.1452935724873896
				],
				[
					7.1509512962436474,
					2.1452935724873896
				],
				[
					7.1509512962436474,
					2.5028356815566895
				],
				[
					6.793409187174348,
					2.5028356815566895
				],
				[
					6.793409187174348,
					3.217933539052467
				],
				[
					6.078297690321278,
					3.217933539052467
				],
				[
					5.720755581251979,
					3.5754756481218237
				],
				[
					5.363213472182679,
					4.2905735056175445
				],
				[
					4.648129254044079,
					4.2905735056175445
				],
				[
					5.005671363113379,
					4.2905735056175445
				],
				[
					5.363213472182679,
					4.2905735056175445
				],
				[
					5.720755581251979,
					4.2905735056175445
				],
				[
					6.435867078105048,
					4.2905735056175445
				],
				[
					6.793409187174348,
					4.2905735056175445
				],
				[
					7.866035514382247,
					4.2905735056175445
				],
				[
					8.581147011235089,
					4.648115614686844
				],
				[
					8.938689120304502,
					4.648115614686844
				],
				[
					9.296231229373802,
					5.005671363113379
				],
				[
					10.011342726226758,
					5.005671363113379
				],
				[
					10.011342726226758,
					5.7207692206091565
				],
				[
					10.368884835296058,
					5.7207692206091565
				],
				[
					10.368884835296058,
					6.078311329678456
				],
				[
					11.083969053434657,
					6.078311329678456
				],
				[
					11.083969053434657,
					6.793409187174234
				],
				[
					10.726426944365357,
					6.793409187174234
				],
				[
					10.368884835296058,
					7.150951296243534
				],
				[
					9.653773338443102,
					7.866049153739368
				],
				[
					9.296231229373802,
					8.223591262808668
				],
				[
					8.938689120304502,
					8.223591262808668
				],
				[
					8.223604902165789,
					8.581147011235146
				],
				[
					7.866035514382247,
					8.581147011235146
				],
				[
					7.1509512962436474,
					9.296244868730923
				],
				[
					6.793409187174348,
					9.653786977800223
				],
				[
					6.078297690321278,
					9.653786977800223
				],
				[
					5.720755581251979,
					10.368884835296058
				],
				[
					5.363213472182679,
					10.368884835296058
				],
				[
					4.648129254044079,
					10.368884835296058
				],
				[
					4.290559866260423,
					10.368884835296058
				],
				[
					3.5754756481218237,
					10.368884835296058
				],
				[
					3.217933539052524,
					10.368884835296058
				],
				[
					2.5028220421995684,
					10.368884835296058
				],
				[
					2.5028220421995684,
					10.368884835296058
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 131,
			"versionNonce": 1979961139,
			"isDeleted": false,
			"id": "IB_iUaGbp5H2ghUmQRika",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 771.5142624233731,
			"y": 359.7944974297766,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 23.955730488358768,
			"height": 18.592462458747548,
			"seed": 360735832,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7151387755673113,
					-0.35754210906929984
				],
				[
					1.0726536059221417,
					-0.35754210906929984
				],
				[
					1.787737824060855,
					-0.7150842181385997
				],
				[
					2.1453072118445107,
					-0.7150842181385997
				],
				[
					2.8603914299831104,
					-1.4301820756344341
				],
				[
					3.57547564812171,
					-1.7877378240609119
				],
				[
					4.290614423689021,
					-2.5028220421995684
				],
				[
					5.363213472182679,
					-2.8603777906259893
				],
				[
					6.07835224774999,
					-3.5754756481218237
				],
				[
					7.150951296243534,
					-4.290559866260423
				],
				[
					8.223604902165789,
					-5.005657723756201
				],
				[
					9.296258508088044,
					-6.078297690321278
				],
				[
					10.3689121140103,
					-6.435853438747813
				],
				[
					11.7990805502875,
					-7.5084934053128904
				],
				[
					12.871734156209868,
					-8.581133371877968
				],
				[
					13.944387762132123,
					-9.653773338443102
				],
				[
					15.017041368054379,
					-10.01132908686958
				],
				[
					16.089640416548036,
					-11.083969053434657
				],
				[
					16.804779192115348,
					-12.156609019999792
				],
				[
					17.877378240608778,
					-12.51416476842627
				],
				[
					18.950031846531147,
					-13.944346844060647
				],
				[
					20.022685452453402,
					-14.659444701556481
				],
				[
					20.380254840237058,
					-15.732084668121558
				],
				[
					21.452853888730715,
					-16.089640416548036
				],
				[
					22.167992664298026,
					-16.447182525617336
				],
				[
					22.167992664298026,
					-17.16228038311317
				],
				[
					22.525507494652857,
					-17.51982249218247
				],
				[
					22.883076882436626,
					-17.51982249218247
				],
				[
					22.883076882436626,
					-18.234920349678248
				],
				[
					23.598161100575226,
					-18.234920349678248
				],
				[
					23.598161100575226,
					-18.592462458747548
				],
				[
					23.955730488358768,
					-18.592462458747548
				],
				[
					23.955730488358768,
					-18.592462458747548
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 146,
			"versionNonce": 944386429,
			"isDeleted": false,
			"id": "ZellHSAql0Mk29NExVA7U",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 794.3973393058097,
			"y": 341.20203497102904,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 12.514164768426213,
			"height": 5.720755581251979,
			"seed": 694305624,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.072653605922369,
					-0.7150978574957776
				],
				[
					-1.430222993705911,
					-0.7150978574957776
				],
				[
					-2.1453072118446244,
					-0.7150978574957776
				],
				[
					-2.5028220421995684,
					-0.7150978574957776
				],
				[
					-3.2179608177668797,
					-0.7150978574957776
				],
				[
					-3.5754756481218237,
					-0.35755574842647775
				],
				[
					-4.648129254044079,
					-0.35755574842647775
				],
				[
					-5.005698641827848,
					0
				],
				[
					-5.720782859966448,
					0
				],
				[
					-6.435867078105048,
					0.7150842181386565
				],
				[
					-7.1509512962436474,
					0.7150842181386565
				],
				[
					-7.508520684027303,
					1.0726399665650774
				],
				[
					-8.223604902165903,
					1.0726399665650774
				],
				[
					-8.223604902165903,
					1.7877378240609119
				],
				[
					-8.581174289949558,
					1.7877378240609119
				],
				[
					-8.581174289949558,
					2.1452799331302117
				],
				[
					-9.296258508088158,
					2.1452799331302117
				],
				[
					-8.938689120304502,
					2.1452799331302117
				],
				[
					-8.581174289949558,
					2.1452799331302117
				],
				[
					-7.508520684027303,
					1.4301820756343773
				],
				[
					-6.79343646588859,
					1.4301820756343773
				],
				[
					-6.435867078105048,
					1.0726399665650774
				],
				[
					-6.078297690321278,
					1.0726399665650774
				],
				[
					-5.363213472182679,
					0.35754210906929984
				],
				[
					-5.005698641827848,
					0
				],
				[
					-3.9330450359054794,
					0
				],
				[
					-3.5754756481218237,
					-0.7150978574957776
				],
				[
					-2.860391429983224,
					-0.7150978574957776
				],
				[
					-2.5028220421995684,
					-1.0726536059223122
				],
				[
					-1.7877378240609687,
					-1.0726536059223122
				],
				[
					-1.7877378240609687,
					-1.430195714991612
				],
				[
					-1.430222993705911,
					-1.430195714991612
				],
				[
					-0.7150842181385997,
					-1.430195714991612
				],
				[
					-0.35756938778376934,
					-1.430195714991612
				],
				[
					-0.35756938778376934,
					-1.0726536059223122
				],
				[
					0,
					-0.35755574842647775
				],
				[
					0.7150842181385997,
					0
				],
				[
					0.7150842181385997,
					0.7150842181386565
				],
				[
					0.7150842181385997,
					1.0726399665650774
				],
				[
					1.0726536059221417,
					1.7877378240609119
				],
				[
					1.0726536059221417,
					2.1452799331302117
				],
				[
					1.787737824060855,
					2.1452799331302117
				],
				[
					1.787737824060855,
					2.5028220421995115
				],
				[
					2.145252654415799,
					3.217919899695289
				],
				[
					2.8603914299831104,
					3.575475648121767
				],
				[
					3.2179062603380544,
					3.575475648121767
				],
				[
					3.2179062603380544,
					4.290559866260367
				],
				[
					3.2179062603380544,
					4.290559866260367
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 148,
			"versionNonce": 1841918163,
			"isDeleted": false,
			"id": "rqAD4n1NT2dBLOcG_qcT6",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 910.2427284819839,
			"y": 401.2700231316035,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 36.46984069935638,
			"height": 13.586818374348525,
			"seed": 54934872,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.357514830354944,
					0
				],
				[
					-0.7150842181385997,
					0
				],
				[
					-1.4301684362771994,
					0
				],
				[
					-1.7877378240609687,
					0
				],
				[
					-2.8603914299831104,
					0
				],
				[
					-3.217906260338168,
					0
				],
				[
					-4.290559866260423,
					0
				],
				[
					-5.363213472182679,
					0
				],
				[
					-6.435867078105048,
					-0.35754210906929984
				],
				[
					-7.508466126598478,
					-0.35754210906929984
				],
				[
					-8.938689120304389,
					-1.0726536059223122
				],
				[
					-10.368857556581702,
					-1.0726536059223122
				],
				[
					-11.441511162503957,
					-1.430195714991612
				],
				[
					-12.871679598781157,
					-2.1452799331302117
				],
				[
					-14.659417422842125,
					-2.1452799331302117
				],
				[
					-16.089640416548036,
					-2.5028220421995115
				],
				[
					-17.16229402247029,
					-3.217933539052467
				],
				[
					-18.592462458747605,
					-3.217933539052467
				],
				[
					-19.307546676886204,
					-3.575475648121767
				],
				[
					-20.022630895024804,
					-3.575475648121767
				],
				[
					-20.737769670592115,
					-3.575475648121767
				],
				[
					-21.09528450094706,
					-3.9330177571910667
				],
				[
					-21.81036871908566,
					-3.9330177571910667
				],
				[
					-21.81036871908566,
					-4.648129254044022
				],
				[
					-22.167938106869315,
					-4.648129254044022
				],
				[
					-22.883022325007914,
					-4.648129254044022
				],
				[
					-23.24059171279157,
					-5.005671363113322
				],
				[
					-24.313245318713825,
					-5.720755581251979
				],
				[
					-24.670760149068883,
					-5.720755581251979
				],
				[
					-25.385844367207483,
					-6.078297690321278
				],
				[
					-25.743413754991025,
					-6.078297690321278
				],
				[
					-26.100983142774794,
					-6.793409187174291
				],
				[
					-26.816067360913394,
					-7.150951296243591
				],
				[
					-27.88872096683565,
					-7.5084934053128904
				],
				[
					-28.246235797190593,
					-8.223604902165846
				],
				[
					-28.961320015329193,
					-8.581147011235146
				],
				[
					-29.676458790896504,
					-9.296231229373745
				],
				[
					-30.74905783939016,
					-9.653773338443045
				],
				[
					-31.821711445312303,
					-10.011342726226701
				],
				[
					-32.89436505123467,
					-11.083969053434657
				],
				[
					-33.25193443901833,
					-11.799080550287613
				],
				[
					-33.96701865715693,
					-11.799080550287613
				],
				[
					-34.32453348751187,
					-12.156622659356913
				],
				[
					-35.03967226307918,
					-12.156622659356913
				],
				[
					-35.39718709343424,
					-12.87170687749557
				],
				[
					-35.75475648121778,
					-12.87170687749557
				],
				[
					-35.75475648121778,
					-13.229248986564869
				],
				[
					-36.46984069935638,
					-13.229248986564869
				],
				[
					-36.46984069935638,
					-13.586818374348525
				],
				[
					-36.46984069935638,
					-13.586818374348525
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 150,
			"versionNonce": 1113651677,
			"isDeleted": false,
			"id": "vaubOlya-2_La_ZByL_oh",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 859.1134158023567,
			"y": 383.03508914256815,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 7.866090071810959,
			"height": 9.296244868730923,
			"seed": 623100248,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.7150842181385997
				],
				[
					0,
					-1.0726399665651343
				],
				[
					0,
					-1.4301820756344341
				],
				[
					0,
					-2.1452799331302117
				],
				[
					0.7151387755673113,
					-2.5028220421995115
				],
				[
					1.0726536059222553,
					-2.5028220421995115
				],
				[
					1.0726536059222553,
					-3.217919899695289
				],
				[
					1.787737824060855,
					-3.217919899695289
				],
				[
					2.1453072118445107,
					-3.217919899695289
				],
				[
					2.1453072118445107,
					-3.5754756481218237
				],
				[
					2.50287659962828,
					-3.5754756481218237
				],
				[
					3.2179608177668797,
					-4.290559866260423
				],
				[
					3.57547564812171,
					-4.290559866260423
				],
				[
					4.290614423689021,
					-4.290559866260423
				],
				[
					4.290614423689021,
					-3.9330177571911236
				],
				[
					4.648129254044079,
					-3.5754756481218237
				],
				[
					4.648129254044079,
					-2.8603777906259893
				],
				[
					4.648129254044079,
					-2.5028220421995115
				],
				[
					4.648129254044079,
					-1.7877378240609119
				],
				[
					4.648129254044079,
					-1.4301820756344341
				],
				[
					4.648129254044079,
					-1.0726399665651343
				],
				[
					4.648129254044079,
					-0.35754210906929984
				],
				[
					3.9330450359054794,
					0
				],
				[
					3.9330450359054794,
					0.7150978574957776
				],
				[
					3.9330450359054794,
					1.0726536059222553
				],
				[
					3.9330450359054794,
					1.4301957149915552
				],
				[
					3.57547564812171,
					2.1452935724873896
				],
				[
					2.8603914299831104,
					2.5028356815566895
				],
				[
					2.8603914299831104,
					3.217947178409645
				],
				[
					2.50287659962828,
					3.217947178409645
				],
				[
					2.50287659962828,
					3.575489287478945
				],
				[
					2.1453072118445107,
					3.575489287478945
				],
				[
					1.430222993705911,
					3.575489287478945
				],
				[
					1.0726536059222553,
					4.2905735056175445
				],
				[
					1.0726536059222553,
					4.648115614686844
				],
				[
					0.35756938778365566,
					4.648115614686844
				],
				[
					0.35756938778365566,
					5.0056850024705
				],
				[
					0.7151387755673113,
					5.0056850024705
				],
				[
					1.0726536059222553,
					5.0056850024705
				],
				[
					1.787737824060855,
					5.0056850024705
				],
				[
					2.1453072118445107,
					5.0056850024705
				],
				[
					2.50287659962828,
					5.0056850024705
				],
				[
					3.2179608177668797,
					5.0056850024705
				],
				[
					4.290614423689021,
					5.0056850024705
				],
				[
					4.648129254044079,
					5.0056850024705
				],
				[
					5.005698641827735,
					5.0056850024705
				],
				[
					5.720782859966334,
					5.0056850024705
				],
				[
					6.07835224774999,
					5.0056850024705
				],
				[
					6.79343646588859,
					5.0056850024705
				],
				[
					7.150951296243534,
					5.0056850024705
				],
				[
					7.866090071810959,
					5.0056850024705
				],
				[
					7.866090071810959,
					5.0056850024705
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 175,
			"versionNonce": 1269423731,
			"isDeleted": false,
			"id": "DWnj4l3sx_JqFBe4dEXwz",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 858.040816753863,
			"y": 376.24169359475104,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 48.984060025211306,
			"height": 32.89437869059179,
			"seed": 2085080920,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.35755574842647775
				],
				[
					-0.35756938778354197,
					-0.35755574842647775
				],
				[
					-0.35756938778354197,
					-1.0726399665650774
				],
				[
					-1.0726536059221417,
					-1.0726399665650774
				],
				[
					-1.430222993705911,
					-1.0726399665650774
				],
				[
					-2.1453072118445107,
					-1.4301957149915552
				],
				[
					-3.217960817766766,
					-1.787737824060855
				],
				[
					-3.9330450359053657,
					-2.5028356815566895
				],
				[
					-5.005698641827621,
					-2.8603777906259893
				],
				[
					-6.07835224774999,
					-3.9330313965482446
				],
				[
					-7.15095129624342,
					-4.648115614686844
				],
				[
					-8.223604902165789,
					-4.648115614686844
				],
				[
					-9.296258508088044,
					-5.005671363113379
				],
				[
					-10.011342726226644,
					-5.363213472182679
				],
				[
					-11.0839963321489,
					-6.078311329678456
				],
				[
					-12.871734156209868,
					-7.508507044670068
				],
				[
					-13.944387762132123,
					-8.223591262808668
				],
				[
					-15.374556198409323,
					-8.581147011235089
				],
				[
					-16.447209804331578,
					-9.653786977800223
				],
				[
					-17.877378240608778,
					-10.726426944365357
				],
				[
					-18.234947628392547,
					-10.726426944365357
				],
				[
					-20.022685452453402,
					-11.799066910930435
				],
				[
					-21.095339058375657,
					-12.514164768426213
				],
				[
					-21.4528538887306,
					-13.229262625922047
				],
				[
					-21.810423276514257,
					-13.586804734991347
				],
				[
					-22.525507494652857,
					-13.586804734991347
				],
				[
					-22.883076882436626,
					-14.301902592487068
				],
				[
					-23.598161100575226,
					-14.659458340913602
				],
				[
					-24.670814706497367,
					-15.374542559052202
				],
				[
					-25.028329536852425,
					-15.73209830747868
				],
				[
					-25.38589892463608,
					-16.089640416548036
				],
				[
					-26.10098314277468,
					-16.804738274043757
				],
				[
					-27.173636748696936,
					-17.162280383113057
				],
				[
					-27.53120613648059,
					-17.87737824060889
				],
				[
					-28.246290354619305,
					-18.23493398903537
				],
				[
					-28.961374572757904,
					-19.307573955600446
				],
				[
					-30.749112396818646,
					-20.38021392216558
				],
				[
					-31.106681784602415,
					-20.38021392216558
				],
				[
					-31.46419661495736,
					-20.73775603123488
				],
				[
					-33.251934439018214,
					-22.525493855295736
				],
				[
					-33.60950382680187,
					-22.525493855295736
				],
				[
					-34.682157432724125,
					-22.88304960372227
				],
				[
					-35.397241650862725,
					-23.24059171279157
				],
				[
					-36.469895256785094,
					-23.955689570287348
				],
				[
					-36.82741008714004,
					-24.313231679356647
				],
				[
					-37.18497947492369,
					-25.028329536852425
				],
				[
					-38.25763308084595,
					-25.028329536852425
				],
				[
					-38.97271729898455,
					-25.38588528527896
				],
				[
					-39.33023212933949,
					-26.10096950341756
				],
				[
					-40.045370904906804,
					-26.10096950341756
				],
				[
					-40.40288573526186,
					-26.458525251844037
				],
				[
					-40.7604551230454,
					-26.458525251844037
				],
				[
					-40.7604551230454,
					-26.816067360913337
				],
				[
					-41.475539341184,
					-26.816067360913337
				],
				[
					-41.83310872896777,
					-26.816067360913337
				],
				[
					-41.83310872896777,
					-27.531165218409114
				],
				[
					-42.54819294710637,
					-27.531165218409114
				],
				[
					-42.54819294710637,
					-27.888707327478414
				],
				[
					-43.26327716524497,
					-28.60380518497425
				],
				[
					-43.97836138338357,
					-28.60380518497425
				],
				[
					-44.33593077116723,
					-28.961360933400726
				],
				[
					-45.05101498930583,
					-29.318903042470026
				],
				[
					-45.40858437708948,
					-29.318903042470026
				],
				[
					-45.40858437708948,
					-30.034000899965804
				],
				[
					-46.12366859522808,
					-30.391543009035104
				],
				[
					-46.12366859522808,
					-31.106640866530938
				],
				[
					-46.48118342558314,
					-31.106640866530938
				],
				[
					-46.83875281336668,
					-31.106640866530938
				],
				[
					-46.83875281336668,
					-31.464182975600238
				],
				[
					-47.55383703150528,
					-31.464182975600238
				],
				[
					-47.55383703150528,
					-32.179280833096016
				],
				[
					-47.91140641928905,
					-32.179280833096016
				],
				[
					-47.91140641928905,
					-32.53683658152249
				],
				[
					-48.62649063742765,
					-32.53683658152249
				],
				[
					-48.62649063742765,
					-32.89437869059179
				],
				[
					-48.984060025211306,
					-32.89437869059179
				],
				[
					-48.984060025211306,
					-32.89437869059179
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 148,
			"versionNonce": 54507069,
			"isDeleted": false,
			"id": "9lX2PH4aiDKdPorweBqvg",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 807.9841576801582,
			"y": 342.2746749375941,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 9.653773338442988,
			"height": 8.581147011235203,
			"seed": 2064280152,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.7150978574957776
				],
				[
					0,
					-0.3575557484264209
				],
				[
					0,
					0
				],
				[
					0,
					0.7150978574958344
				],
				[
					0,
					1.0726399665651343
				],
				[
					0,
					1.4301820756344341
				],
				[
					0.7150842181385997,
					2.1452799331302117
				],
				[
					1.0725990484935437,
					3.217919899695289
				],
				[
					1.0725990484935437,
					3.5754756481218237
				],
				[
					1.0725990484935437,
					4.648115614686901
				],
				[
					1.787737824060855,
					4.648115614686901
				],
				[
					1.787737824060855,
					5.005657723756201
				],
				[
					1.787737824060855,
					5.720755581251979
				],
				[
					2.145252654415799,
					6.078311329678513
				],
				[
					2.145252654415799,
					5.363213472182679
				],
				[
					2.145252654415799,
					5.005657723756201
				],
				[
					1.4301684362771994,
					4.648115614686901
				],
				[
					1.4301684362771994,
					3.9330177571911236
				],
				[
					1.4301684362771994,
					3.5754756481218237
				],
				[
					1.4301684362771994,
					2.8603777906259893
				],
				[
					1.4301684362771994,
					1.7877378240609119
				],
				[
					1.4301684362771994,
					1.4301820756344341
				],
				[
					1.4301684362771994,
					1.0726399665651343
				],
				[
					1.4301684362771994,
					0
				],
				[
					1.4301684362771994,
					-0.7150978574957776
				],
				[
					1.4301684362771994,
					-1.0726399665650774
				],
				[
					1.4301684362771994,
					-1.787737824060855
				],
				[
					1.4301684362771994,
					-2.1452935724873896
				],
				[
					1.4301684362771994,
					-2.5028356815566895
				],
				[
					1.787737824060855,
					-2.5028356815566895
				],
				[
					2.145252654415799,
					-2.5028356815566895
				],
				[
					2.8603368725543987,
					-2.5028356815566895
				],
				[
					2.8603368725543987,
					-2.1452935724873896
				],
				[
					3.217906260338168,
					-2.1452935724873896
				],
				[
					3.57547564812171,
					-2.1452935724873896
				],
				[
					3.57547564812171,
					-1.4301957149915552
				],
				[
					4.29055986626031,
					-1.4301957149915552
				],
				[
					4.648074696615367,
					-1.4301957149915552
				],
				[
					5.363213472182679,
					-1.0726399665650774
				],
				[
					5.720728302537623,
					-1.0726399665650774
				],
				[
					6.4358125206762224,
					-1.0726399665650774
				],
				[
					6.4358125206762224,
					-0.3575557484264209
				],
				[
					6.793381908459878,
					-0.3575557484264209
				],
				[
					7.150951296243534,
					-0.3575557484264209
				],
				[
					7.866035514382247,
					-0.3575557484264209
				],
				[
					8.223550344737077,
					-0.3575557484264209
				],
				[
					8.938689120304389,
					-0.3575557484264209
				],
				[
					9.296203950659446,
					-0.3575557484264209
				],
				[
					9.653773338442988,
					-0.3575557484264209
				],
				[
					9.653773338442988,
					-0.3575557484264209
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 114,
			"versionNonce": 443258899,
			"isDeleted": false,
			"id": "FK4wj4gObEvdhUPjNNZmS",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 809.0567567286517,
			"y": 339.7718392560374,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 2.8603368725545124,
			"height": 3.217919899695346,
			"seed": 1551593048,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.7150978574957207
				],
				[
					-0.357514830354944,
					-0.7150978574957207
				],
				[
					-0.357514830354944,
					-1.0726399665650774
				],
				[
					-1.0725990484935437,
					-1.0726399665650774
				],
				[
					-1.4301684362771994,
					-1.0726399665650774
				],
				[
					-1.787737824060855,
					-1.0726399665650774
				],
				[
					-2.5028220421994547,
					-1.0726399665650774
				],
				[
					-2.8603368725545124,
					-1.0726399665650774
				],
				[
					-2.8603368725545124,
					-0.35754210906929984
				],
				[
					-2.1452526544159127,
					-0.35754210906929984
				],
				[
					-2.1452526544159127,
					0
				],
				[
					-1.787737824060855,
					0.7150978574958344
				],
				[
					-1.4301684362771994,
					1.0726399665651343
				],
				[
					-0.7150842181385997,
					1.430195714991612
				],
				[
					-0.357514830354944,
					2.1452799331302685
				],
				[
					-0.357514830354944,
					2.1452799331302685
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 108,
			"versionNonce": 1170728605,
			"isDeleted": false,
			"id": "3omhOcCkNVzfvrLJW3sJm",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 826.219050751122,
			"y": 324.3972966969852,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 3.9330450359054794,
			"height": 0.35755574842647775,
			"seed": 1717438552,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.35755574842647775
				],
				[
					0.35756938778365566,
					-0.35755574842647775
				],
				[
					1.072653605922369,
					-0.35755574842647775
				],
				[
					1.430222993705911,
					-0.35755574842647775
				],
				[
					1.7877378240609687,
					-0.35755574842647775
				],
				[
					2.5028220421995684,
					-0.35755574842647775
				],
				[
					2.8603914299831104,
					-0.35755574842647775
				],
				[
					3.57547564812171,
					-0.35755574842647775
				],
				[
					3.9330450359054794,
					-0.35755574842647775
				],
				[
					3.9330450359054794,
					-0.35755574842647775
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 108,
			"versionNonce": 1208294835,
			"isDeleted": false,
			"id": "gJ7vbQRBh8z7-wjmUs5Cz",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 827.2917043570444,
			"y": 327.97277234510705,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 4.29055986626031,
			"height": 0,
			"seed": 2049393752,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.35756938778354197,
					0
				],
				[
					0.7150842181385997,
					0
				],
				[
					1.4301684362771994,
					0
				],
				[
					1.7877378240607413,
					0
				],
				[
					2.502822042199341,
					0
				],
				[
					2.8603914299831104,
					0
				],
				[
					3.57547564812171,
					0
				],
				[
					3.9330450359053657,
					0
				],
				[
					4.29055986626031,
					0
				],
				[
					4.29055986626031,
					0
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 115,
			"versionNonce": 2091584253,
			"isDeleted": false,
			"id": "YbQ8i_o9-zstGUw2Rn_nM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 840.8511962959047,
			"y": 320.38864079565485,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 4.2201216920294655,
			"height": 0,
			"seed": 1339198808,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.4219949974838073,
					0
				],
				[
					0.5626743064110542,
					0
				],
				[
					0.8440114596165813,
					0
				],
				[
					0.9846907685437145,
					0
				],
				[
					1.1253486128221084,
					0
				],
				[
					1.5473650749547687,
					0
				],
				[
					1.8287022281602958,
					0
				],
				[
					1.9693815370875427,
					0
				],
				[
					2.25071869029307,
					0
				],
				[
					2.391397999220203,
					0
				],
				[
					2.813414461352977,
					0
				],
				[
					2.9540723056312572,
					0
				],
				[
					3.2354094588367843,
					0
				],
				[
					3.376088767764031,
					0
				],
				[
					3.6574259209695583,
					0
				],
				[
					3.798105229896805,
					0
				],
				[
					3.9387630741750854,
					0
				],
				[
					4.2201216920294655,
					0
				],
				[
					4.079442383102219,
					0
				],
				[
					3.9387630741750854,
					0
				],
				[
					3.9387630741750854,
					0
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 199,
			"versionNonce": 1067249491,
			"isDeleted": false,
			"id": "3a1HT6yCTy6D0ltwyUUP5",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 839.4444890652283,
			"y": 320.2479668528899,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 7.174193997660723,
			"height": 9.002928422794469,
			"seed": 1449186600,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.1406739427649768
				],
				[
					0,
					0.42201646213271715
				],
				[
					0,
					0.5626850387354807
				],
				[
					0,
					0.844027558103221
				],
				[
					0,
					0.9846961347059846
				],
				[
					0,
					1.266038654073725
				],
				[
					0,
					1.4067072306764885
				],
				[
					0,
					1.5473811734414653
				],
				[
					0,
					1.8287236928092057
				],
				[
					0,
					1.9693922694119692
				],
				[
					0,
					2.2507347887797096
				],
				[
					0,
					2.391403365382473
				],
				[
					0,
					2.53207730814745
				],
				[
					0,
					2.813414461352977
				],
				[
					0,
					2.954088404117954
				],
				[
					0,
					3.235430923485694
				],
				[
					0,
					3.3760995000884577
				],
				[
					0,
					3.657442019456198
				],
				[
					0,
					3.7981105960589616
				],
				[
					0,
					3.9387845388239953
				],
				[
					0,
					4.2201216920294655
				],
				[
					0,
					4.360795634794442
				],
				[
					0,
					4.642138154162183
				],
				[
					0.1406578442782802,
					4.642138154162183
				],
				[
					0.4219949974838073,
					4.642138154162183
				],
				[
					0.5626743064110542,
					4.642138154162183
				],
				[
					0.8440114596165813,
					4.501464211397206
				],
				[
					0.9846907685437145,
					4.501464211397206
				],
				[
					1.2660279217492416,
					4.501464211397206
				],
				[
					1.4067072306764885,
					4.360795634794442
				],
				[
					1.5473650749547687,
					4.360795634794442
				],
				[
					1.8287022281602958,
					4.079453115426702
				],
				[
					1.9693815370875427,
					4.079453115426702
				],
				[
					2.25071869029307,
					3.9387845388239953
				],
				[
					2.532055843498597,
					3.9387845388239953
				],
				[
					2.813414461352977,
					3.9387845388239953
				],
				[
					3.2354094588367843,
					3.9387845388239953
				],
				[
					3.376088767764031,
					3.9387845388239953
				],
				[
					3.7981052298966915,
					3.9387845388239953
				],
				[
					3.9387630741750854,
					3.9387845388239953
				],
				[
					4.2201216920294655,
					3.9387845388239953
				],
				[
					4.360779536307746,
					3.9387845388239953
				],
				[
					4.642116689513273,
					3.9387845388239953
				],
				[
					5.204812460573294,
					3.9387845388239953
				],
				[
					5.345470304851574,
					4.2201216920294655
				],
				[
					5.626828922705954,
					4.2201216920294655
				],
				[
					5.767486766984234,
					4.360795634794442
				],
				[
					6.048823920189761,
					4.360795634794442
				],
				[
					6.189503229117008,
					4.360795634794442
				],
				[
					6.470840382322535,
					4.360795634794442
				],
				[
					6.6115196912496685,
					4.360795634794442
				],
				[
					6.6115196912496685,
					4.642138154162183
				],
				[
					6.752177535528062,
					4.642138154162183
				],
				[
					6.752177535528062,
					4.782806730765003
				],
				[
					7.0335361533824425,
					4.782806730765003
				],
				[
					7.0335361533824425,
					5.064149250132743
				],
				[
					7.174193997660723,
					5.20481782673545
				],
				[
					7.174193997660723,
					5.345491769500484
				],
				[
					7.174193997660723,
					5.626828922705954
				],
				[
					7.174193997660723,
					5.767502865470988
				],
				[
					7.174193997660723,
					6.048845384838728
				],
				[
					7.174193997660723,
					6.189513961441492
				],
				[
					7.174193997660723,
					6.330182538044198
				],
				[
					7.174193997660723,
					6.611525057411939
				],
				[
					7.174193997660723,
					6.752199000176972
				],
				[
					7.174193997660723,
					7.033536153382499
				],
				[
					6.892856844455309,
					7.174210096147476
				],
				[
					6.892856844455309,
					7.4555526155152165
				],
				[
					6.752177535528062,
					7.4555526155152165
				],
				[
					6.752177535528062,
					7.59622119211798
				],
				[
					6.6115196912496685,
					7.59622119211798
				],
				[
					6.6115196912496685,
					7.736889768720744
				],
				[
					6.330182538044255,
					7.736889768720744
				],
				[
					6.189503229117008,
					7.736889768720744
				],
				[
					6.189503229117008,
					8.018232288088484
				],
				[
					5.908166075911481,
					8.15890623085346
				],
				[
					5.767486766984234,
					8.440243384058988
				],
				[
					5.486149613778707,
					8.440243384058988
				],
				[
					5.345470304851574,
					8.580917326823965
				],
				[
					5.204812460573294,
					8.580917326823965
				],
				[
					4.923475307367653,
					8.580917326823965
				],
				[
					4.78279599844052,
					8.580917326823965
				],
				[
					4.501458845234993,
					8.862259846191705
				],
				[
					4.360779536307746,
					8.862259846191705
				],
				[
					4.360779536307746,
					9.002928422794469
				],
				[
					4.079442383102219,
					9.002928422794469
				],
				[
					3.9387630741750854,
					9.002928422794469
				],
				[
					3.7981052298966915,
					9.002928422794469
				],
				[
					3.516768076691278,
					9.002928422794469
				],
				[
					3.376088767764031,
					9.002928422794469
				],
				[
					3.094751614558504,
					9.002928422794469
				],
				[
					2.9540723056312572,
					9.002928422794469
				],
				[
					2.67273515242573,
					9.002928422794469
				],
				[
					2.391397999220203,
					9.002928422794469
				],
				[
					1.9693815370875427,
					9.002928422794469
				],
				[
					1.6880443838820156,
					9.002928422794469
				],
				[
					1.4067072306764885,
					9.002928422794469
				],
				[
					1.1253486128221084,
					9.002928422794469
				],
				[
					0.9846907685437145,
					9.002928422794469
				],
				[
					0.7033536153381874,
					9.002928422794469
				],
				[
					0.5626743064110542,
					9.002928422794469
				],
				[
					0.2813371532055271,
					9.002928422794469
				],
				[
					0.1406578442782802,
					9.002928422794469
				],
				[
					0.4219949974838073,
					9.002928422794469
				],
				[
					0.8440114596165813,
					9.002928422794469
				],
				[
					0.8440114596165813,
					9.002928422794469
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "ellipse",
			"version": 345,
			"versionNonce": 1214948189,
			"isDeleted": false,
			"id": "jPONP7vZw29xN-46hlRmV",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dotted",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 788.0767579133444,
			"y": 408.01691761416174,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 235.06324954187428,
			"height": 118.87025394077342,
			"seed": 975858008,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 147,
			"versionNonce": 1133087987,
			"isDeleted": false,
			"id": "k6N3kdm5",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dotted",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 796.3593564710466,
			"y": 445.2024068197113,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 74.63996887207031,
			"height": 40,
			"seed": 1940247592,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Same as \nOthers",
			"rawText": "Same as \nOthers",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Same as \nOthers",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1534,
			"versionNonce": 1140299357,
			"isDeleted": false,
			"id": "q0K6-cpKbgMPB8F5wNOG5",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1101.8240342471922,
			"y": -376.39890390772825,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 810.7795986610721,
			"height": 542.2523373967291,
			"seed": 1787969622,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421700090,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 1260,
			"versionNonce": 122779283,
			"isDeleted": false,
			"id": "N5xzVXeM",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1112.3181397439616,
			"y": -338.2843617398254,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 625.043701171875,
			"height": 35,
			"seed": 922635786,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": " How to understand and approach a problem ",
			"rawText": " How to understand and approach a problem ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": " How to understand and approach a problem ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1223,
			"versionNonce": 1771384861,
			"isDeleted": false,
			"id": "YneffLUi",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1106.3236675475719,
			"y": -240.75774091919666,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 370.67181396484375,
			"height": 40,
			"seed": 613810698,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# Identify if you can break down problem into \nsmaller problems",
			"rawText": "# Identify if you can break down problem into \nsmaller problems",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# Identify if you can break down problem into \nsmaller problems",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1251,
			"versionNonce": 162212915,
			"isDeleted": false,
			"id": "jnwLVCBt",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1118.6962261413216,
			"y": -179.11964015887307,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 330.43182373046875,
			"height": 20,
			"seed": 1847508170,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# Write down recurrent relation if needed",
			"rawText": "# Write down recurrent relation if needed",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# Write down recurrent relation if needed",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1204,
			"versionNonce": 454239357,
			"isDeleted": false,
			"id": "SbOdzVSu",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1120.8372936462044,
			"y": -136.75774091919675,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 212.59188842773438,
			"height": 20,
			"seed": 173729238,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# Draw the recursive tree",
			"rawText": "# Draw the recursive tree",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# Draw the recursive tree",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1387,
			"versionNonce": 779955667,
			"isDeleted": false,
			"id": "42HSEtpP",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1213.13730114791,
			"y": -94.99984921916382,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 312.2558288574219,
			"height": 100,
			"seed": 744439318,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# About the tree :-\n-> See the flow of functions, how they \nare getting in stack ...\n-> Identify the flow of left and right \ntree calls ...",
			"rawText": "# About the tree :-\n-> See the flow of functions, how they \nare getting in stack ...\n-> Identify the flow of left and right \ntree calls ...",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# About the tree :-\n-> See the flow of functions, how they \nare getting in stack ...\n-> Identify the flow of left and right \ntree calls ...",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1471,
			"versionNonce": 181833875,
			"isDeleted": false,
			"id": "GuVLaSAY",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1109.9595936674536,
			"y": 51.11372054629314,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 420.351806640625,
			"height": 60,
			"seed": 2087276438,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421702665,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# See how th e values are returned at each step.\nSee where two function call will come out of, In the \nend you will come out of the main function ...",
			"rawText": "# See how th e values are returned at each step.\nSee where two function call will come out of, In the \nend you will come out of the main function ...",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# See how th e values are returned at each step.\nSee where two function call will come out of, In the \nend you will come out of the main function ...",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 342,
			"versionNonce": 417201011,
			"isDeleted": false,
			"id": "n5GqKKyL7AthvQ6f4N2Op",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dotted",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1524.501756267014,
			"y": -257.27408675988505,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 79.40051743460435,
			"height": 380.04341637368026,
			"seed": 1865661322,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.5417347799293566,
					0
				],
				[
					2.312660983305932,
					0
				],
				[
					3.854395763235516,
					1.5417641866353904
				],
				[
					5.3961305431648725,
					2.312660983306074
				],
				[
					9.250526306400388,
					4.625292559906171
				],
				[
					10.79231989974187,
					6.16705674654159
				],
				[
					14.646715662977385,
					7.708791526471003
				],
				[
					16.95931783287142,
					10.021452509777077
				],
				[
					20.042846206142258,
					11.56318728970652
				],
				[
					22.35550718944819,
					13.875848273012593
				],
				[
					24.668109359342452,
					14.646715662977329
				],
				[
					26.209902952683706,
					16.959347239577426
				],
				[
					30.835224919295797,
					20.042875612848235
				],
				[
					34.68962068253131,
					22.355507189448332
				],
				[
					34.68962068253131,
					23.126374579413067
				],
				[
					36.2313554624609,
					24.668138766048457
				],
				[
					38.54401644576683,
					26.980770342648583
				],
				[
					38.54401644576683,
					27.751667139319267
				],
				[
					40.08575122569641,
					27.751667139319267
				],
				[
					40.08575122569641,
					29.293431325954657
				],
				[
					40.856559802249194,
					30.064298715919364
				],
				[
					40.856559802249194,
					30.8351661058841
				],
				[
					42.398412209002345,
					32.37693029251949
				],
				[
					42.398412209002345,
					33.14782708919017
				],
				[
					42.398412209002345,
					34.689561869119586
				],
				[
					42.398412209002345,
					35.46045866579027
				],
				[
					42.398412209002345,
					37.773090242390396
				],
				[
					42.398412209002345,
					40.08572181899052
				],
				[
					42.398412209002345,
					40.856618615661176
				],
				[
					42.398412209002345,
					43.1692501922613
				],
				[
					42.398412209002345,
					46.252749158826134
				],
				[
					42.398412209002345,
					50.878041718732334
				],
				[
					42.398412209002345,
					53.961540685297166
				],
				[
					42.398412209002345,
					56.27420166860324
				],
				[
					42.398412209002345,
					60.128597431838756
				],
				[
					42.398412209002345,
					63.21209639840359
				],
				[
					42.398412209002345,
					66.29562477167437
				],
				[
					42.398412209002345,
					68.6082563482745
				],
				[
					42.398412209002345,
					71.69178472154528
				],
				[
					42.398412209002345,
					74.00441629814537
				],
				[
					42.398412209002345,
					77.0879152647102
				],
				[
					42.398412209002345,
					79.4005762480163
				],
				[
					42.398412209002345,
					80.94231102794572
				],
				[
					42.398412209002345,
					82.48407521458114
				],
				[
					42.398412209002345,
					84.79670679118124
				],
				[
					42.398412209002345,
					86.33847097781666
				],
				[
					42.398412209002345,
					88.65110255441675
				],
				[
					41.62748600562577,
					90.19286674105217
				],
				[
					41.62748600562577,
					92.50549831765227
				],
				[
					41.62748600562577,
					94.04726250428769
				],
				[
					41.62748600562577,
					95.58902669092305
				],
				[
					41.62748600562577,
					97.9016582675232
				],
				[
					41.62748600562577,
					100.2142898441233
				],
				[
					42.398412209002345,
					101.75605403075872
				],
				[
					42.398412209002345,
					103.29781821739408
				],
				[
					43.16922078555535,
					105.61044979399423
				],
				[
					43.16922078555535,
					107.92308137059433
				],
				[
					43.94014698893193,
					110.23574235390038
				],
				[
					43.94014698893193,
					112.54837393050053
				],
				[
					43.94014698893193,
					114.86100550710063
				],
				[
					45.481881768861285,
					117.17363708370073
				],
				[
					45.481881768861285,
					118.71540127033614
				],
				[
					45.481881768861285,
					121.02803284693624
				],
				[
					46.25280797223786,
					122.56979703357166
				],
				[
					46.25280797223786,
					124.11156122020702
				],
				[
					46.25280797223786,
					126.42419279680718
				],
				[
					46.25280797223786,
					128.73682437340727
				],
				[
					47.79454275216722,
					130.2785885600427
				],
				[
					47.79454275216722,
					131.82035274667805
				],
				[
					48.565351328720226,
					134.1329843232782
				],
				[
					48.565351328720226,
					135.67474850991357
				],
				[
					48.565351328720226,
					136.4456158998783
				],
				[
					48.565351328720226,
					137.98738008651372
				],
				[
					48.565351328720226,
					138.7582474764784
				],
				[
					50.10720373547338,
					141.0709084597845
				],
				[
					50.10720373547338,
					141.84177584974918
				],
				[
					50.10720373547338,
					144.15440742634934
				],
				[
					50.10720373547338,
					144.92530422302002
				],
				[
					50.10720373547338,
					146.46703900294943
				],
				[
					50.10720373547338,
					148.77969998625554
				],
				[
					50.878012312026385,
					149.55056737622022
				],
				[
					50.878012312026385,
					151.09233156285563
				],
				[
					51.64893851540273,
					151.86319895282037
				],
				[
					51.64893851540273,
					152.63409574949105
				],
				[
					53.19067329533232,
					154.17583052942047
				],
				[
					53.19067329533232,
					154.94672732609115
				],
				[
					53.96159949870889,
					156.4884915127265
				],
				[
					53.96159949870889,
					157.25935890269125
				],
				[
					55.50333427863825,
					158.80112308932667
				],
				[
					56.27414285519126,
					160.34288727596203
				],
				[
					57.04506905856783,
					161.8846220558915
				],
				[
					59.357730041873765,
					162.65551885256218
				],
				[
					60.89946482180335,
					164.96815042916228
				],
				[
					63.21212580510928,
					166.5099146157977
				],
				[
					63.98293438166229,
					168.05167880243306
				],
				[
					66.29559536496845,
					169.59341358236253
				],
				[
					68.60825634827438,
					170.3643103790332
				],
				[
					69.37918255165096,
					171.90607456566858
				],
				[
					70.92091733158031,
					171.90607456566858
				],
				[
					71.69172590813332,
					171.90607456566858
				],
				[
					71.69172590813332,
					172.6769419556333
				],
				[
					72.4626521115099,
					172.6769419556333
				],
				[
					74.00438689143948,
					172.6769419556333
				],
				[
					74.77531309481583,
					172.6769419556333
				],
				[
					76.31704787474541,
					173.44780934559805
				],
				[
					77.08797407812199,
					173.44780934559805
				],
				[
					78.62970885805134,
					173.44780934559805
				],
				[
					79.40051743460435,
					173.44780934559805
				],
				[
					77.858782654675,
					174.9895735322334
				],
				[
					77.08797407812199,
					177.30220510883356
				],
				[
					74.77531309481583,
					178.0731019055042
				],
				[
					71.69172590813332,
					180.38573348210434
				],
				[
					70.14999112820396,
					182.69836505870444
				],
				[
					69.37918255165096,
					185.01099663530454
				],
				[
					67.8373301448978,
					187.32365761861064
				],
				[
					67.0665215683448,
					188.09452500857537
				],
				[
					65.52478678841544,
					190.40715658517547
				],
				[
					65.52478678841544,
					192.71978816177557
				],
				[
					64.75386058503886,
					194.261552348411
				],
				[
					64.75386058503886,
					196.57418392501108
				],
				[
					64.75386058503886,
					198.8868449083172
				],
				[
					63.98293438166229,
					201.19947648491728
				],
				[
					63.98293438166229,
					203.51210806151738
				],
				[
					63.98293438166229,
					204.28297545148212
				],
				[
					62.44119960173293,
					208.13737121471763
				],
				[
					62.44119960173293,
					211.2208995879884
				],
				[
					62.44119960173293,
					213.53353116458857
				],
				[
					62.44119960173293,
					214.3044279612592
				],
				[
					62.44119960173293,
					217.38792692782403
				],
				[
					62.44119960173293,
					219.70055850442418
				],
				[
					62.44119960173293,
					222.78408687769496
				],
				[
					63.21212580510928,
					225.09671845429506
				],
				[
					63.98293438166229,
					228.95111421753057
				],
				[
					64.75386058503886,
					232.03464259080135
				],
				[
					64.75386058503886,
					235.1181709640722
				],
				[
					66.29559536496845,
					237.43077313396634
				],
				[
					67.0665215683448,
					240.51430150723712
				],
				[
					68.60825634827438,
					242.82696249054317
				],
				[
					69.37918255165096,
					245.910490863814
				],
				[
					70.92091733158031,
					248.22309303370815
				],
				[
					70.92091733158031,
					250.5357540170142
				],
				[
					70.92091733158031,
					253.61928239028504
				],
				[
					71.69172590813332,
					255.93188456017918
				],
				[
					71.69172590813332,
					258.24454554348523
				],
				[
					71.69172590813332,
					260.5571477133794
				],
				[
					71.69172590813332,
					262.8698086966855
				],
				[
					71.69172590813332,
					265.1824696799915
				],
				[
					71.69172590813332,
					266.724204459921
				],
				[
					71.69172590813332,
					270.5786002231565
				],
				[
					71.69172590813332,
					272.1203350030859
				],
				[
					71.69172590813332,
					278.28739174962755
				],
				[
					71.69172590813332,
					279.0582591395922
				],
				[
					71.69172590813332,
					283.6835222927925
				],
				[
					71.69172590813332,
					284.4544484961691
				],
				[
					71.69172590813332,
					287.537918056028
				],
				[
					71.69172590813332,
					292.16324002264014
				],
				[
					69.37918255165096,
					297.55937056580507
				],
				[
					69.37918255165096,
					300.64289893907585
				],
				[
					67.8373301448978,
					302.95550110897005
				],
				[
					65.52478678841544,
					306.8098968722055
				],
				[
					64.75386058503886,
					309.89342524547635
				],
				[
					63.98293438166229,
					312.2060862287824
				],
				[
					62.44119960173293,
					315.2896146020532
				],
				[
					61.670391025179924,
					317.6022167719474
				],
				[
					60.128538618426774,
					319.9148777552534
				],
				[
					59.357730041873765,
					321.45661253518284
				],
				[
					57.81599526194441,
					323.76927351848894
				],
				[
					57.04506905856783,
					325.31100829841836
				],
				[
					56.27414285519126,
					327.6236692817244
				],
				[
					56.27414285519126,
					328.3945366716892
				],
				[
					54.7324080752619,
					329.1654040616539
				],
				[
					54.7324080752619,
					331.4780650449599
				],
				[
					53.96159949870889,
					333.0197998248894
				],
				[
					53.96159949870889,
					335.33246080819544
				],
				[
					53.96159949870889,
					336.1033281981602
				],
				[
					52.41974709195574,
					336.8741955881249
				],
				[
					51.64893851540273,
					338.4159891814663
				],
				[
					51.64893851540273,
					339.18685657143095
				],
				[
					51.64893851540273,
					340.7285913513604
				],
				[
					50.878012312026385,
					341.4994587413251
				],
				[
					50.878012312026385,
					343.04125233466647
				],
				[
					49.3362775320968,
					343.81211972463126
				],
				[
					49.3362775320968,
					344.58298711459594
				],
				[
					48.565351328720226,
					346.1247807079373
				],
				[
					48.565351328720226,
					346.895648097902
				],
				[
					47.02361654879087,
					348.43738287783145
				],
				[
					47.02361654879087,
					349.20825026779613
				],
				[
					47.02361654879087,
					349.9791764711728
				],
				[
					46.25280797223786,
					351.5209112511023
				],
				[
					46.25280797223786,
					352.29177864106697
				],
				[
					44.71095556548471,
					353.83357223440834
				],
				[
					44.71095556548471,
					354.604439624373
				],
				[
					43.94014698893193,
					356.1461744043025
				],
				[
					43.94014698893193,
					356.91704179426716
				],
				[
					43.16922078555535,
					357.68796799764385
				],
				[
					43.16922078555535,
					359.2297027775733
				],
				[
					41.62748600562577,
					359.2297027775733
				],
				[
					41.62748600562577,
					360.000570167538
				],
				[
					40.856559802249194,
					360.000570167538
				],
				[
					40.856559802249194,
					361.54236376087937
				],
				[
					39.31482502231984,
					362.31323115084405
				],
				[
					38.54401644576683,
					362.31323115084405
				],
				[
					37.00216403901368,
					363.8549659307735
				],
				[
					36.2313554624609,
					364.6258333207382
				],
				[
					35.46042925908432,
					364.6258333207382
				],
				[
					35.46042925908432,
					365.3967595241149
				],
				[
					33.91869447915474,
					365.3967595241149
				],
				[
					33.14776827577816,
					366.93849430404424
				],
				[
					31.606033495848806,
					366.93849430404424
				],
				[
					30.835224919295797,
					367.70936169400903
				],
				[
					30.06429871591922,
					367.70936169400903
				],
				[
					28.522563935989865,
					369.2511552873504
				],
				[
					27.75163773261329,
					369.2511552873504
				],
				[
					26.209902952683706,
					370.0220226773151
				],
				[
					25.439035562719027,
					370.0220226773151
				],
				[
					23.897241969377774,
					370.0220226773151
				],
				[
					22.35550718944819,
					370.79289006727976
				],
				[
					20.813713596106936,
					370.79289006727976
				],
				[
					20.042846206142258,
					372.3346248472092
				],
				[
					18.501111426212674,
					372.3346248472092
				],
				[
					17.730244036247996,
					372.3346248472092
				],
				[
					17.730244036247996,
					373.1055510505859
				],
				[
					16.188450442906742,
					373.1055510505859
				],
				[
					15.417583052942064,
					373.1055510505859
				],
				[
					14.646715662977385,
					373.1055510505859
				],
				[
					13.104922069635904,
					374.6472858305153
				],
				[
					12.334054679671226,
					374.6472858305153
				],
				[
					10.79231989974187,
					374.6472858305153
				],
				[
					10.021452509776964,
					375.41815322048006
				],
				[
					8.47965891643571,
					376.95994681382143
				],
				[
					7.708791526471032,
					376.95994681382143
				],
				[
					6.9379241365063535,
					377.7308142037861
				],
				[
					5.3961305431648725,
					377.7308142037861
				],
				[
					5.3961305431648725,
					378.5016815937508
				],
				[
					4.625263153200194,
					378.5016815937508
				],
				[
					4.625263153200194,
					380.04341637368026
				],
				[
					6.167056746541448,
					380.04341637368026
				],
				[
					6.9379241365063535,
					380.04341637368026
				],
				[
					6.9379241365063535,
					380.04341637368026
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 230,
			"versionNonce": 1755834685,
			"isDeleted": false,
			"id": "peCeEojF",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dotted",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1625.847975547711,
			"y": -96.16033209395829,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 219.53587341308594,
			"height": 40,
			"seed": 1478839882,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Follow these steps to \nsolve any recursion problem ",
			"rawText": "Follow these steps to \nsolve any recursion problem ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Follow these steps to \nsolve any recursion problem ",
			"lineHeight": 1.25
		},
		{
			"type": "ellipse",
			"version": 661,
			"versionNonce": 1158944019,
			"isDeleted": false,
			"id": "MJKYqrVg7mAtSXSyxxTrX",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1825.0873784984797,
			"y": -351.7023763476656,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 80.9803541126721,
			"height": 85.47926267448713,
			"seed": 1260698326,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "sRA96vkQ"
				}
			],
			"updated": 1715421158215,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 587,
			"versionNonce": 1437710749,
			"isDeleted": false,
			"id": "sRA96vkQ",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1856.7946763595905,
			"y": -326.68422815440005,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 17.304000854492188,
			"height": 35,
			"seed": 1404235798,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "5",
			"rawText": "5",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MJKYqrVg7mAtSXSyxxTrX",
			"originalText": "5",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1586,
			"versionNonce": 1653996211,
			"isDeleted": false,
			"id": "DRrp_nIdZvx26BOw_1iGi",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1105.9942021634697,
			"y": 226.26873645752323,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 810.7795986610721,
			"height": 542.2523373967291,
			"seed": 1204090506,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 1435,
			"versionNonce": 904035837,
			"isDeleted": false,
			"id": "TN1Dffvn",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1358.5665768361714,
			"y": 257.97544094208,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 188.35589599609375,
			"height": 35,
			"seed": 230266186,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Binary Search",
			"rawText": "Binary Search",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Binary Search",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 2138,
			"versionNonce": 1846160467,
			"isDeleted": false,
			"id": "eV7Fd9dP",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1125.0737543469784,
			"y": 307.283573405846,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 150.58969116210938,
			"height": 16.45431046882485,
			"seed": 652281610,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 13.16344837505988,
			"fontFamily": 1,
			"text": "# F(N) = O(1) + F(N/2)",
			"rawText": "# F(N) = O(1) + F(N/2)",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# F(N) = O(1) + F(N/2)",
			"lineHeight": 1.25
		},
		{
			"type": "ellipse",
			"version": 822,
			"versionNonce": 1882961501,
			"isDeleted": false,
			"id": "vBQzaBp2toLPWvcNSrGlf",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1814.3060609520178,
			"y": 244.55742633423972,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 80.9803541126721,
			"height": 85.47926267448713,
			"seed": 540552010,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "0SxsfI4O"
				}
			],
			"updated": 1715421158215,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 751,
			"versionNonce": 189213171,
			"isDeleted": false,
			"id": "0SxsfI4O",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1845.705360155902,
			"y": 269.5755745275053,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 17.919998168945312,
			"height": 35,
			"seed": 57160202,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "6",
			"rawText": "6",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vBQzaBp2toLPWvcNSrGlf",
			"originalText": "6",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 480,
			"versionNonce": 261022397,
			"isDeleted": false,
			"id": "ntcjdCn2fyh5csFQUuC1G",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1137.7805069968354,
			"y": 297.5652010555918,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 169.28522214328711,
			"height": 35.66878648568848,
			"seed": 550517962,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 489,
			"versionNonce": 525562771,
			"isDeleted": false,
			"id": "GmQ3DVLb",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1331.1023721802364,
			"y": 327.0060904737978,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 115.39991760253906,
			"height": 16.45431046882485,
			"seed": 2064193738,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"fontSize": 13.16344837505988,
			"fontFamily": 1,
			"text": "Recursive realtion",
			"rawText": "Recursive realtion",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Recursive realtion",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 483,
			"versionNonce": 1216185117,
			"isDeleted": false,
			"id": "S_fPF05pmCUwwVibUPPDp",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1305.9334038530535,
			"y": 330.40313112816654,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 37.36729601401266,
			"height": 10.75726300892023,
			"seed": 259261590,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.6984879306037157,
					0
				],
				[
					2.2646505741383374,
					0.5661842412550128
				],
				[
					3.9631817001828353,
					0.5661842412550128
				],
				[
					5.095506987251929,
					1.1323468847895597
				],
				[
					6.227875469761955,
					1.1323468847895597
				],
				[
					7.360200756831048,
					2.2646937695791194
				],
				[
					7.926363400365671,
					2.2646937695791194
				],
				[
					9.058731882875696,
					2.2646937695791194
				],
				[
					9.058731882875696,
					2.830856413113704
				],
				[
					9.624894526410168,
					2.830856413113704
				],
				[
					10.757219813479411,
					2.830856413113704
				],
				[
					11.323425652454816,
					2.830856413113704
				],
				[
					11.889588295989288,
					2.830856413113704
				],
				[
					13.02191358305853,
					2.830856413113704
				],
				[
					14.720444709103178,
					3.9632032979032634
				],
				[
					15.28660735263765,
					3.9632032979032634
				],
				[
					16.418932639706743,
					4.529387539158276
				],
				[
					16.9851384786823,
					4.529387539158276
				],
				[
					17.55130112221677,
					4.529387539158276
				],
				[
					18.683626409285864,
					4.529387539158276
				],
				[
					19.249789052820486,
					4.529387539158276
				],
				[
					20.38215753533036,
					5.095550182692823
				],
				[
					20.94832017886513,
					5.095550182692823
				],
				[
					21.514482822399604,
					5.095550182692823
				],
				[
					22.64685130490963,
					5.095550182692823
				],
				[
					23.213013948444253,
					5.095550182692823
				],
				[
					24.345339235513197,
					6.227897067482383
				],
				[
					24.911501879047968,
					6.227897067482383
				],
				[
					26.043870361557843,
					6.227897067482383
				],
				[
					26.610033005092316,
					6.227897067482383
				],
				[
					27.176195648627086,
					6.227897067482383
				],
				[
					28.30856413113696,
					6.227897067482383
				],
				[
					28.30856413113696,
					5.661712826227408
				],
				[
					28.874726774671586,
					5.661712826227408
				],
				[
					28.874726774671586,
					5.095550182692823
				],
				[
					28.874726774671586,
					4.529387539158276
				],
				[
					28.874726774671586,
					3.3970406543686793
				],
				[
					28.874726774671586,
					2.830856413113704
				],
				[
					28.874726774671586,
					1.6985311260445723
				],
				[
					27.74235829216156,
					1.1323468847895597
				],
				[
					27.176195648627086,
					0
				],
				[
					26.610033005092316,
					0
				],
				[
					25.47770771802337,
					0
				],
				[
					26.043870361557843,
					0
				],
				[
					26.610033005092316,
					0
				],
				[
					26.610033005092316,
					0.5661842412550128
				],
				[
					27.176195648627086,
					0.5661842412550128
				],
				[
					28.30856413113696,
					1.1323468847895597
				],
				[
					28.874726774671586,
					1.1323468847895597
				],
				[
					30.00705206174068,
					2.2646937695791194
				],
				[
					30.573214705275152,
					2.2646937695791194
				],
				[
					30.573214705275152,
					2.830856413113704
				],
				[
					31.705583187785326,
					2.830856413113704
				],
				[
					32.2717458313198,
					3.9632032979032634
				],
				[
					32.837908474854274,
					3.9632032979032634
				],
				[
					33.97027695736445,
					3.9632032979032634
				],
				[
					34.536439600898916,
					4.529387539158276
				],
				[
					35.66876488796816,
					5.095550182692823
				],
				[
					36.234927531502635,
					5.095550182692823
				],
				[
					36.234927531502635,
					6.227897067482383
				],
				[
					37.36729601401266,
					6.227897067482383
				],
				[
					36.801133370478034,
					6.227897067482383
				],
				[
					36.234927531502635,
					6.227897067482383
				],
				[
					35.10260224443354,
					6.227897067482383
				],
				[
					34.536439600898916,
					6.227897067482383
				],
				[
					33.40407111838904,
					6.227897067482383
				],
				[
					32.837908474854274,
					6.227897067482383
				],
				[
					32.2717458313198,
					6.794059711016967
				],
				[
					31.139420544250704,
					6.794059711016967
				],
				[
					30.573214705275152,
					7.926406595806527
				],
				[
					28.874726774671586,
					7.926406595806527
				],
				[
					28.874726774671586,
					8.492569239341075
				],
				[
					27.74235829216156,
					8.492569239341075
				],
				[
					27.176195648627086,
					9.624916124130634
				],
				[
					26.610033005092316,
					9.624916124130634
				],
				[
					25.47770771802337,
					10.191100365385646
				],
				[
					24.911501879047968,
					10.191100365385646
				],
				[
					24.911501879047968,
					10.75726300892023
				],
				[
					23.779176591978725,
					10.75726300892023
				],
				[
					23.779176591978725,
					10.75726300892023
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 477,
			"versionNonce": 711297331,
			"isDeleted": false,
			"id": "9PgYhSN1sexED48fSi4Mt",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1213.6474675073707,
			"y": 322.47674613008047,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 15.852813191613203,
			"height": 32.83793007257477,
			"seed": 468275018,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158215,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.5661626435345843
				],
				[
					0,
					2.264672171858691
				],
				[
					0,
					2.830856413113704
				],
				[
					0,
					3.397019056648288
				],
				[
					0,
					5.095528584972395
				],
				[
					-0.5661626435346218,
					6.227875469761955
				],
				[
					-0.5661626435346218,
					6.794059711016967
				],
				[
					-1.6985311260446472,
					8.492569239341112
				],
				[
					-2.2646937695791194,
					10.757241411199802
				],
				[
					-3.397019056648363,
					12.455772537244375
				],
				[
					-3.9631817001828353,
					14.720444709103067
				],
				[
					-5.09555018269286,
					15.852791593892626
				],
				[
					-5.6617128262274825,
					16.418954237427172
				],
				[
					-5.6617128262274825,
					17.55130112221673
				],
				[
					-5.6617128262274825,
					18.117485363471744
				],
				[
					-6.227875469761955,
					18.68364800700633
				],
				[
					-6.227875469761955,
					19.81599489179589
				],
				[
					-6.227875469761955,
					20.382157535330435
				],
				[
					-7.36024395227198,
					21.514504420119994
				],
				[
					-7.36024395227198,
					22.08066706365458
				],
				[
					-7.9264065958066015,
					23.21301394844414
				],
				[
					-7.9264065958066015,
					23.77919818969915
				],
				[
					-9.058731882875696,
					24.3453608332337
				],
				[
					-9.058731882875696,
					25.47770771802326
				],
				[
					-9.058731882875696,
					26.043870361557843
				],
				[
					-9.624894526410317,
					26.043870361557843
				],
				[
					-9.624894526410317,
					27.176217246347402
				],
				[
					-10.19110036538572,
					28.30856413113696
				],
				[
					-10.19110036538572,
					29.440911015926524
				],
				[
					-11.323425652454816,
					29.440911015926524
				],
				[
					-11.323425652454816,
					30.007073659461106
				],
				[
					-11.323425652454816,
					31.139420544250665
				],
				[
					-11.889588295989437,
					31.139420544250665
				],
				[
					-11.889588295989437,
					31.705583187785212
				],
				[
					-13.021956778499312,
					30.573236302995653
				],
				[
					-13.021956778499312,
					30.007073659461106
				],
				[
					-13.021956778499312,
					28.874726774671547
				],
				[
					-13.588119422033934,
					28.30856413113696
				],
				[
					-13.588119422033934,
					27.74237988988195
				],
				[
					-13.588119422033934,
					26.61005460281282
				],
				[
					-13.588119422033934,
					26.043870361557843
				],
				[
					-14.72044470910303,
					26.043870361557843
				],
				[
					-14.72044470910303,
					24.911523476768284
				],
				[
					-15.28660735263765,
					24.911523476768284
				],
				[
					-15.28660735263765,
					24.3453608332337
				],
				[
					-15.852813191613203,
					23.77919818969915
				],
				[
					-15.852813191613203,
					24.3453608332337
				],
				[
					-15.852813191613203,
					25.47770771802326
				],
				[
					-15.852813191613203,
					26.043870361557843
				],
				[
					-15.28660735263765,
					27.176217246347402
				],
				[
					-15.28660735263765,
					27.74237988988195
				],
				[
					-15.28660735263765,
					28.30856413113696
				],
				[
					-14.154282065568557,
					28.30856413113696
				],
				[
					-14.154282065568557,
					29.440911015926524
				],
				[
					-14.154282065568557,
					30.007073659461106
				],
				[
					-14.154282065568557,
					31.139420544250665
				],
				[
					-13.588119422033934,
					31.705583187785212
				],
				[
					-13.588119422033934,
					32.83793007257477
				],
				[
					-12.45575093952391,
					32.83793007257477
				],
				[
					-12.45575093952391,
					32.271767429040224
				],
				[
					-12.45575093952391,
					31.705583187785212
				],
				[
					-11.889588295989437,
					30.573236302995653
				],
				[
					-10.757263008920193,
					30.007073659461106
				],
				[
					-10.19110036538572,
					28.874726774671547
				],
				[
					-9.624894526410317,
					28.874726774671547
				],
				[
					-8.492569239341075,
					28.30856413113696
				],
				[
					-7.9264065958066015,
					28.30856413113696
				],
				[
					-7.9264065958066015,
					27.74237988988195
				],
				[
					-6.794038113296576,
					27.74237988988195
				],
				[
					-6.227875469761955,
					26.61005460281282
				],
				[
					-5.6617128262274825,
					26.61005460281282
				],
				[
					-4.529387539158239,
					26.61005460281282
				],
				[
					-4.529387539158239,
					26.043870361557843
				],
				[
					-3.9631817001828353,
					26.043870361557843
				],
				[
					-3.9631817001828353,
					26.043870361557843
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 461,
			"versionNonce": 1064900477,
			"isDeleted": false,
			"id": "5LuaFveO",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1127.7238382828016,
			"y": 356.58855294946824,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 100.91078186035156,
			"height": 16.45431046882485,
			"seed": 2007844502,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 13.16344837505988,
			"fontFamily": 1,
			"text": "Comparison time",
			"rawText": "Comparison time",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Comparison time",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 472,
			"versionNonce": 1642326739,
			"isDeleted": false,
			"id": "P1u6XiAt",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1248.2087519039458,
			"y": 368.62674333886326,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 77.18931579589844,
			"height": 28.978961640838964,
			"seed": 566277898,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 11.591584656335586,
			"fontFamily": 1,
			"text": "Dividing array\nin half",
			"rawText": "Dividing array\nin half",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Dividing array\nin half",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 504,
			"versionNonce": 247668701,
			"isDeleted": false,
			"id": "PaElnsm_kleLUzuJ_VF21",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1273.4015579983668,
			"y": 324.94100024382067,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 15.614982791151393,
			"height": 37.475964655406834,
			"seed": 630816278,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.3123008471516768
				],
				[
					0,
					0.9368965848117933
				],
				[
					0,
					1.24919743196347
				],
				[
					0,
					1.8737991262668237
				],
				[
					0,
					2.1860999734185005
				],
				[
					0,
					2.810695711078617
				],
				[
					0,
					3.1229965582302937
				],
				[
					0,
					3.4352974053819705
				],
				[
					0,
					4.059893143042087
				],
				[
					0,
					4.372193990193764
				],
				[
					0,
					4.996795684497117
				],
				[
					0,
					5.933692269308948
				],
				[
					0,
					6.245993116460587
				],
				[
					0,
					7.182889701272418
				],
				[
					0,
					8.11979224272741
				],
				[
					-0.6246136075897528,
					9.056688827539242
				],
				[
					-0.6246136075897528,
					9.681290521842595
				],
				[
					-0.6246136075897528,
					10.618187106654387
				],
				[
					-0.6246136075897528,
					11.867384538617857
				],
				[
					-0.6246136075897528,
					12.491986232921212
				],
				[
					-0.6246136075897528,
					13.428882817733005
				],
				[
					-0.6246136075897528,
					14.365785359188035
				],
				[
					-0.6246136075897528,
					14.678086206339712
				],
				[
					-0.6246136075897528,
					15.614982791151505
				],
				[
					-0.6246136075897528,
					16.5518793759633
				],
				[
					-0.6246136075897528,
					16.864180223114975
				],
				[
					-0.6246136075897528,
					18.113377655078445
				],
				[
					-0.6246136075897528,
					19.987176781345305
				],
				[
					-0.31231871708135056,
					21.236374213308775
				],
				[
					0,
					24.04707588103063
				],
				[
					0.6245897810169542,
					25.92086905065422
				],
				[
					0.6245897810169542,
					27.170072439260924
				],
				[
					0.6245897810169542,
					28.10696902407272
				],
				[
					0.9368846715253565,
					29.04386560888451
				],
				[
					0.9368846715253565,
					29.98076815033954
				],
				[
					0.9368846715253565,
					30.29306899749122
				],
				[
					1.249179562033759,
					31.22996558230301
				],
				[
					1.249179562033759,
					32.16686216711481
				],
				[
					1.249179562033759,
					33.103764708569834
				],
				[
					1.249179562033759,
					33.41606555572151
				],
				[
					1.249179562033759,
					34.04066129338167
				],
				[
					1.249179562033759,
					34.35296809717654
				],
				[
					1.249179562033759,
					34.66526298768498
				],
				[
					1.8737931696236614,
					35.289864681988334
				],
				[
					1.8737931696236614,
					35.602159572496774
				],
				[
					1.8737931696236614,
					36.226761266800125
				],
				[
					1.5614982791151093,
					35.914466376291685
				],
				[
					1.5614982791151093,
					35.602159572496774
				],
				[
					1.249179562033759,
					35.602159572496774
				],
				[
					1.249179562033759,
					34.97755787819346
				],
				[
					0.9368846715253565,
					34.35296809717654
				],
				[
					0.3122948905084023,
					33.728360446229985
				],
				[
					0,
					33.41606555572151
				],
				[
					-0.6246136075897528,
					32.79146386141816
				],
				[
					-1.561498279115259,
					31.854567276606364
				],
				[
					-1.87381699619646,
					31.54226642945469
				],
				[
					-2.1861118867048623,
					31.22996558230301
				],
				[
					-2.8107016677218164,
					30.60536388799966
				],
				[
					-3.747610165820121,
					30.29306899749122
				],
				[
					-5.309108444935231,
					29.04386560888451
				],
				[
					-6.245993116460587,
					28.10696902407272
				],
				[
					-6.870606724050489,
					27.482367329769364
				],
				[
					-8.119810112657047,
					27.170072439260924
				],
				[
					-8.119810112657047,
					26.54547074495757
				],
				[
					-8.4321050031656,
					26.54547074495757
				],
				[
					-8.4321050031656,
					26.233169897805894
				],
				[
					-9.056694784182403,
					26.233169897805894
				],
				[
					-8.744399893674002,
					26.85777159210925
				],
				[
					-7.807491395575696,
					27.170072439260924
				],
				[
					-7.182901614558892,
					28.10696902407272
				],
				[
					-6.245993116460587,
					28.73157071837607
				],
				[
					-5.309108444935231,
					29.35616645603619
				],
				[
					-4.372199946837076,
					30.29306899749122
				],
				[
					-3.1229965582303683,
					31.54226642945469
				],
				[
					-2.498406777213414,
					32.16686216711481
				],
				[
					-1.87381699619646,
					32.47916301426648
				],
				[
					-0.9369084980983048,
					33.41606555572151
				],
				[
					0,
					34.35296809717654
				],
				[
					0.6245897810169542,
					34.66526298768498
				],
				[
					0.9368846715253565,
					35.289864681988334
				],
				[
					0.9368846715253565,
					35.602159572496774
				],
				[
					1.249179562033759,
					35.602159572496774
				],
				[
					1.249179562033759,
					36.53905615730861
				],
				[
					1.8737931696236614,
					36.53905615730861
				],
				[
					1.8737931696236614,
					37.16365785161196
				],
				[
					2.1860880601320636,
					37.16365785161196
				],
				[
					2.1860880601320636,
					37.475964655406834
				],
				[
					2.810677841148868,
					37.475964655406834
				],
				[
					3.1229965582303683,
					36.85136296110348
				],
				[
					3.1229965582303683,
					36.53905615730861
				],
				[
					3.747586339247173,
					35.914466376291685
				],
				[
					4.059881229755575,
					35.602159572496774
				],
				[
					4.059881229755575,
					34.97755787819346
				],
				[
					4.99678972785388,
					34.35296809717654
				],
				[
					4.99678972785388,
					33.728360446229985
				],
				[
					5.309084618362283,
					33.728360446229985
				],
				[
					5.933674399379236,
					33.41606555572151
				],
				[
					6.245993116460587,
					32.79146386141816
				],
				[
					6.245993116460587,
					32.47916301426648
				],
				[
					6.558288006968989,
					32.47916301426648
				],
				[
					6.558288006968989,
					31.854567276606364
				],
				[
					6.558288006968989,
					31.854567276606364
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 529,
			"versionNonce": 1155759165,
			"isDeleted": false,
			"id": "DxLatxQR",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1124.7885435593246,
			"y": 433.42357766252843,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 361.9678039550781,
			"height": 80,
			"seed": 2101872726,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421174961,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": " # if you want to apply binary search on \nan array of size n, take a step that takes \nconstant amount of time + search in \nhalf of the array ",
			"rawText": " # if you want to apply binary search on \nan array of size n, take a step that takes \nconstant amount of time + search in \nhalf of the array ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": " # if you want to apply binary search on \nan array of size n, take a step that takes \nconstant amount of time + search in \nhalf of the array ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 701,
			"versionNonce": 1168520285,
			"isDeleted": false,
			"id": "0egKluFl",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1136.4570602635915,
			"y": 597.2261562454913,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 297.5797424316406,
			"height": 25,
			"seed": 1911488150,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421401378,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Types of recurrent relations :",
			"rawText": "Types of recurrent relations :",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Types of recurrent relations :",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 686,
			"versionNonce": 251240637,
			"isDeleted": false,
			"id": "LU3lD7mv",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1164.0953033658361,
			"y": 636.4095527128796,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 349.05584716796875,
			"height": 60,
			"seed": 1323006090,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421401378,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "(1) Linear recurrent relations : Fibonacci num\n(2) Divide and conquer : Binary search\n(Returned by a factor) ",
			"rawText": "(1) Linear recurrent relations : Fibonacci num\n(2) Divide and conquer : Binary search\n(Returned by a factor) ",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "(1) Linear recurrent relations : Fibonacci num\n(2) Divide and conquer : Binary search\n(Returned by a factor) ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1056,
			"versionNonce": 1347980445,
			"isDeleted": false,
			"id": "vnNOtLsk",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1487.619396959171,
			"y": 358.06024405800565,
			"strokeColor": "#099268",
			"backgroundColor": "transparent",
			"width": 384.7109375,
			"height": 240.7796827782052,
			"seed": 938914442,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 13.758839015897438,
			"fontFamily": 1,
			"text": "    static int search(int[] arr, int target, int s, int e){\n        if (s > e){\n            return -1;\n        }\n        int m = s + (e-s)/2;\n\n        if(arr[m] == target){\n            return m;\n        }\n        if(target < arr[m]){\n            search(arr, target, s, m-1);\n        }\n        return search(arr, target, m+1, e);\n    }",
			"rawText": "    static int search(int[] arr, int target, int s, int e){\n        if (s > e){\n            return -1;\n        }\n        int m = s + (e-s)/2;\n\n        if(arr[m] == target){\n            return m;\n        }\n        if(target < arr[m]){\n            search(arr, target, s, m-1);\n        }\n        return search(arr, target, m+1, e);\n    }",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "    static int search(int[] arr, int target, int s, int e){\n        if (s > e){\n            return -1;\n        }\n        int m = s + (e-s)/2;\n\n        if(arr[m] == target){\n            return m;\n        }\n        if(target < arr[m]){\n            search(arr, target, s, m-1);\n        }\n        return search(arr, target, m+1, e);\n    }",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 414,
			"versionNonce": 1757009843,
			"isDeleted": false,
			"id": "WkcKM2L3X_sDxZhpaUeId",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1493.9478753545343,
			"y": 348.20122361186355,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 402.4000244140622,
			"height": 265.59997558593744,
			"seed": 232180822,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "freedraw",
			"version": 168,
			"versionNonce": 2050420989,
			"isDeleted": false,
			"id": "12ltmzP09kZ_Sy0gDTOFs",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1643.6449523528747,
			"y": 378.6217248551877,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 228.27833428634062,
			"height": 3.742263972254932,
			"seed": 828887882,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					4.210058121613201,
					0
				],
				[
					4.677834426449181,
					0
				],
				[
					5.145610731285387,
					0
				],
				[
					6.548975334837678,
					0
				],
				[
					7.484527944509864,
					0
				],
				[
					7.952339938390423,
					0
				],
				[
					9.355668852898361,
					0
				],
				[
					9.823445157734568,
					0
				],
				[
					11.226809761287086,
					0
				],
				[
					13.097950669675583,
					0
				],
				[
					15.436867882900287,
					0
				],
				[
					17.308008791288785,
					0
				],
				[
					17.775785096124764,
					0
				],
				[
					20.114702309349468,
					0
				],
				[
					22.92139582741015,
					0
				],
				[
					25.260313040634855,
					0
				],
				[
					32.74484098514472,
					0.46777630483603616
				],
				[
					36.95489910675792,
					0.46777630483603616
				],
				[
					43.97165074643158,
					0.46777630483603616
				],
				[
					48.18170886804478,
					1.4033467590303417
				],
				[
					54.730684202882685,
					1.4033467590303417
				],
				[
					61.27962384867601,
					1.4033467590303417
				],
				[
					72.03865730512712,
					1.4033467590303417
				],
				[
					74.37757451835182,
					1.4033467590303417
				],
				[
					81.86210246286169,
					1.4033467590303417
				],
				[
					90.74999501092407,
					1.4033467590303417
				],
				[
					103.8479099915553,
					1.4033467590303417
				],
				[
					110.39692101543756,
					1.4033467590303417
				],
				[
					113.20357884445389,
					1.4033467590303417
				],
				[
					120.6881424780081,
					1.4033467590303417
				],
				[
					125.83378889833762,
					1.4033467590303417
				],
				[
					137.06056297058035,
					1.4033467590303417
				],
				[
					138.46392757413287,
					1.4033467590303417
				],
				[
					143.14176200058205,
					1.4033467590303417
				],
				[
					146.4162318234787,
					1.4033467590303417
				],
				[
					150.15851364025616,
					1.4033467590303417
				],
				[
					152.96517146927226,
					1.4033467590303417
				],
				[
					154.8363480667051,
					1.4033467590303417
				],
				[
					155.7719006763773,
					1.4033467590303417
				],
				[
					156.23971267025786,
					1.4033467590303417
				],
				[
					156.70745328604949,
					1.4033467590303417
				],
				[
					157.64300589572144,
					1.4033467590303417
				],
				[
					158.11081788960178,
					1.4033467590303417
				],
				[
					159.0463704992742,
					1.4033467590303417
				],
				[
					160.44973510282648,
					1.4033467590303417
				],
				[
					161.38528771249867,
					2.3389172132245903
				],
				[
					162.78865231605118,
					2.3389172132245903
				],
				[
					165.59538152315622,
					2.8066935180606833
				],
				[
					170.74095656539725,
					3.742263972254932
				],
				[
					172.6121331628301,
					3.742263972254932
				],
				[
					174.95105037605458,
					3.742263972254932
				],
				[
					175.4187909918462,
					3.742263972254932
				],
				[
					178.22552019895147,
					3.742263972254932
				],
				[
					180.09662541829562,
					3.742263972254932
				],
				[
					182.90335462540065,
					3.742263972254932
				],
				[
					184.7744598447448,
					3.742263972254932
				],
				[
					185.71001245441698,
					3.742263972254932
				],
				[
					186.64563644217765,
					3.742263972254932
				],
				[
					187.58118905185006,
					3.742263972254932
				],
				[
					188.0489296676417,
					3.742263972254932
				],
				[
					188.98455365540235,
					3.742263972254932
				],
				[
					189.45229427119398,
					3.742263972254932
				],
				[
					189.92010626507454,
					3.742263972254932
				],
				[
					190.85565887474672,
					3.742263972254932
				],
				[
					191.32347086862706,
					3.742263972254932
				],
				[
					192.259023478299,
					3.742263972254932
				],
				[
					193.66238808185176,
					3.742263972254932
				],
				[
					194.59794069152372,
					3.742263972254932
				],
				[
					196.00130529507624,
					3.742263972254932
				],
				[
					197.40459852054005,
					3.742263972254932
				],
				[
					199.27577511797313,
					3.742263972254932
				],
				[
					200.67913972152542,
					3.742263972254932
				],
				[
					203.48579755054175,
					3.742263972254932
				],
				[
					203.95360954442208,
					3.742263972254932
				],
				[
					206.29252675764678,
					3.742263972254932
				],
				[
					208.16363197699116,
					3.742263972254932
				],
				[
					211.43810179988782,
					3.742263972254932
				],
				[
					211.90591379376815,
					3.742263972254932
				],
				[
					214.7126430008732,
					3.742263972254932
				],
				[
					215.64819561054537,
					3.742263972254932
				],
				[
					216.58374822021756,
					3.742263972254932
				],
				[
					217.51930082988952,
					3.742263972254932
				],
				[
					217.98711282376985,
					3.742263972254932
				],
				[
					218.92266543344203,
					3.742263972254932
				],
				[
					219.3904774273226,
					3.742263972254932
				],
				[
					219.85821804311422,
					3.742263972254932
				],
				[
					220.79377065278618,
					3.742263972254932
				],
				[
					221.2615826466665,
					3.742263972254932
				],
				[
					222.1971352563387,
					3.742263972254932
				],
				[
					222.66494725021926,
					3.742263972254932
				],
				[
					223.60049985989122,
					3.742263972254932
				],
				[
					224.06831185377155,
					3.742263972254932
				],
				[
					224.5360524695634,
					3.742263972254932
				],
				[
					225.4716050792356,
					3.742263972254932
				],
				[
					225.93941707311592,
					3.742263972254932
				],
				[
					226.87496968278788,
					3.742263972254932
				],
				[
					227.34278167666844,
					3.742263972254932
				],
				[
					228.27833428634062,
					3.742263972254932
				],
				[
					228.27833428634062,
					3.742263972254932
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 124,
			"versionNonce": 497707347,
			"isDeleted": false,
			"id": "QKgBLOgPZLii1DfF_OJy1",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1794.7390186028028,
			"y": 381.4284183732484,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 12.162326681914692,
			"height": 17.30799094676661,
			"seed": 1377733898,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.403364603552518
				],
				[
					0,
					2.3389172132245903
				],
				[
					0,
					3.7422818167771084
				],
				[
					0,
					4.210058121613201
				],
				[
					0,
					5.613404880643486
				],
				[
					0,
					6.081199030001699
				],
				[
					0,
					7.016751639673828
				],
				[
					0,
					7.48454578903204
				],
				[
					0,
					8.420116243226346
				],
				[
					0,
					8.887892548062382
				],
				[
					0,
					9.355668852898475
				],
				[
					0,
					10.291239307092724
				],
				[
					0,
					10.759033456450993
				],
				[
					0,
					11.694586066123065
				],
				[
					-0.9355526096719586,
					11.694586066123065
				],
				[
					-0.9355526096719586,
					11.22680976128703
				],
				[
					-1.403364603552518,
					11.22680976128703
				],
				[
					-2.338917213224704,
					10.759033456450993
				],
				[
					-2.806729207105036,
					10.759033456450993
				],
				[
					-3.2744698228966627,
					9.823463002256688
				],
				[
					-4.210022432568849,
					9.355668852898475
				],
				[
					-4.677834426449408,
					8.887892548062382
				],
				[
					-5.613387036121367,
					8.887892548062382
				],
				[
					-6.081199030001699,
					7.952322093868133
				],
				[
					-7.484563633554444,
					7.952322093868133
				],
				[
					-7.484563633554444,
					7.48454578903204
				],
				[
					-7.952304249346071,
					7.48454578903204
				],
				[
					-8.88785685901803,
					7.48454578903204
				],
				[
					-8.420116243226403,
					7.48454578903204
				],
				[
					-7.952304249346071,
					7.48454578903204
				],
				[
					-7.484563633554444,
					7.48454578903204
				],
				[
					-6.081199030001699,
					8.420116243226346
				],
				[
					-5.14564642032974,
					8.887892548062382
				],
				[
					-4.677834426449408,
					10.291239307092724
				],
				[
					-4.677834426449408,
					10.759033456450993
				],
				[
					-3.742281816777222,
					11.694586066123065
				],
				[
					-3.2744698228966627,
					12.630156520317314
				],
				[
					-2.806729207105036,
					14.033503279347656
				],
				[
					-1.871105219344372,
					14.969073733541961
				],
				[
					-1.871105219344372,
					15.436867882900174
				],
				[
					-1.403364603552518,
					16.372420492572303
				],
				[
					-0.467811993880332,
					16.840214641930515
				],
				[
					0,
					17.30799094676661
				],
				[
					0.9355526096719586,
					17.30799094676661
				],
				[
					1.403364603552518,
					17.30799094676661
				],
				[
					1.403364603552518,
					16.840214641930515
				],
				[
					1.8711052193441446,
					15.904644187736267
				],
				[
					2.806729207105036,
					15.436867882900174
				],
				[
					2.806729207105036,
					14.501297428705925
				],
				[
					2.806729207105036,
					14.033503279347656
				],
				[
					3.2744698228966627,
					13.097950669675583
				],
				[
					3.2744698228966627,
					12.630156520317314
				],
				[
					3.2744698228966627,
					12.162380215481335
				],
				[
					3.2744698228966627,
					11.22680976128703
				],
				[
					3.2744698228966627,
					11.22680976128703
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 127,
			"versionNonce": 931776861,
			"isDeleted": false,
			"id": "LwvxQsum",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1759.6552604044334,
			"y": 397.96192165259606,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 78.73594665527344,
			"height": 20,
			"seed": 261140822,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "arguments",
			"rawText": "arguments",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "arguments",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 142,
			"versionNonce": 903333619,
			"isDeleted": false,
			"id": "lYsmPEWGBxxlyTC-BeWN-",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1681.5354040693046,
			"y": 435.2235142774146,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 31.809288375472534,
			"height": 20.582460769663385,
			"seed": 1132392918,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.467811993880332,
					0
				],
				[
					0.9355882987165387,
					0
				],
				[
					1.8711409083884973,
					0
				],
				[
					2.338917213224704,
					0
				],
				[
					3.2745055119412427,
					0
				],
				[
					3.742281816777222,
					0
				],
				[
					5.14564642032974,
					0
				],
				[
					6.548975334837905,
					0
				],
				[
					7.952339938390423,
					0
				],
				[
					8.88789254806261,
					0
				],
				[
					10.2912571516149,
					0
				],
				[
					14.501315273228101,
					0
				],
				[
					16.372420492572473,
					0
				],
				[
					17.775785096124764,
					0
				],
				[
					19.17914969967751,
					0
				],
				[
					19.64692600451349,
					0
				],
				[
					20.582478614185675,
					0
				],
				[
					21.050254919021654,
					0
				],
				[
					21.985843217737965,
					0
				],
				[
					22.453619522574172,
					0
				],
				[
					23.38917213224613,
					0
				],
				[
					23.85698412612669,
					0
				],
				[
					24.32476043096267,
					0
				],
				[
					25.260313040634628,
					0
				],
				[
					25.728089345470835,
					0
				],
				[
					25.728089345470835,
					-0.46777630483603616
				],
				[
					25.728089345470835,
					-0.9355526096721292
				],
				[
					24.792536735798876,
					-0.9355526096721292
				],
				[
					24.32476043096267,
					-1.8711230638663778
				],
				[
					22.92139582741015,
					-3.2744698228967195
				],
				[
					21.518066912901986,
					-3.742263972254989
				],
				[
					20.114702309349468,
					-4.210040277090968
				],
				[
					19.17914969967751,
					-5.145610731285274
				],
				[
					17.775785096124764,
					-5.61338703612131
				],
				[
					16.372420492572473,
					-6.548957490315615
				],
				[
					14.969091578064308,
					-7.016751639673828
				],
				[
					14.501315273228101,
					-7.952304249345957
				],
				[
					13.565726974511563,
					-7.952304249345957
				],
				[
					13.09795066967581,
					-7.952304249345957
				],
				[
					12.162398060003397,
					-7.952304249345957
				],
				[
					12.162398060003397,
					-8.42009839870417
				],
				[
					11.694586066123065,
					-8.42009839870417
				],
				[
					11.694586066123065,
					-8.887874703540263
				],
				[
					12.630174364839604,
					-8.42009839870417
				],
				[
					13.09795066967581,
					-8.42009839870417
				],
				[
					14.03350327934777,
					-7.484527944509921
				],
				[
					15.904644187736267,
					-6.081181185479579
				],
				[
					17.308008791289012,
					-5.61338703612131
				],
				[
					19.17914969967751,
					-4.210040277090968
				],
				[
					21.985843217737965,
					-2.8066935180606265
				],
				[
					23.85698412612669,
					-2.338917213224647
				],
				[
					24.792536735798876,
					-1.4033467590303417
				],
				[
					26.663677644187374,
					-0.9355526096721292
				],
				[
					28.06700655869554,
					0
				],
				[
					29.47037116224783,
					0.4677941493582125
				],
				[
					29.938147467084036,
					0.4677941493582125
				],
				[
					30.405923771920243,
					1.403364603552518
				],
				[
					31.341512070636554,
					1.403364603552518
				],
				[
					31.341512070636554,
					1.8711409083885542
				],
				[
					31.809288375472534,
					1.8711409083885542
				],
				[
					31.809288375472534,
					2.338917213224647
				],
				[
					30.873735765800575,
					2.338917213224647
				],
				[
					30.405923771920243,
					3.274487667418896
				],
				[
					29.938147467084036,
					3.742281816777165
				],
				[
					29.002594857412078,
					3.742281816777165
				],
				[
					28.53481855257587,
					4.6778344264492375
				],
				[
					27.599230253859332,
					5.145628575807507
				],
				[
					25.728089345470835,
					6.5489753348378485
				],
				[
					24.32476043096267,
					7.016751639673828
				],
				[
					22.92139582741015,
					7.952322093868133
				],
				[
					21.985843217737965,
					8.420116243226346
				],
				[
					20.582478614185675,
					9.355668852898475
				],
				[
					19.64692600451349,
					9.823463002256688
				],
				[
					19.17914969967751,
					10.29123930709278
				],
				[
					19.17914969967751,
					11.22680976128703
				],
				[
					18.24356140096097,
					11.22680976128703
				],
				[
					18.24356140096097,
					11.694586066123122
				],
				[
					17.775785096124764,
					11.694586066123122
				],
				[
					17.775785096124764,
					11.694586066123122
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 178,
			"versionNonce": 161650109,
			"isDeleted": false,
			"id": "8i30woIx",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1720.998372104847,
			"y": 423.5289460558137,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 74.882568359375,
			"height": 27.837637629040838,
			"seed": 1290910026,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 11.135055051616336,
			"fontFamily": 1,
			"text": "finding middle \nelements",
			"rawText": "finding middle \nelements",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "finding middle \nelements",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 178,
			"versionNonce": 1204318355,
			"isDeleted": false,
			"id": "2sKis0mkUFAS-wQGZDHsd",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1548.6849349093818,
			"y": 460.6007803165195,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 30.873700076755995,
			"height": 132.3827285441311,
			"seed": 1040440010,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.9355882987165387,
					0
				],
				[
					-0.9355882987165387,
					-0.9355704541943055
				],
				[
					-1.403364603552518,
					-0.9355704541943055
				],
				[
					-1.8711409083884973,
					-0.9355704541943055
				],
				[
					-3.2745055119410154,
					-0.9355704541943055
				],
				[
					-4.677834426449181,
					-0.9355704541943055
				],
				[
					-6.081199030001699,
					-0.9355704541943055
				],
				[
					-6.548975334837905,
					-0.9355704541943055
				],
				[
					-9.355668852898361,
					-0.9355704541943055
				],
				[
					-11.226809761287086,
					-0.9355704541943055
				],
				[
					-12.162398060003397,
					-0.9355704541943055
				],
				[
					-13.565726974511563,
					-0.9355704541943055
				],
				[
					-14.501315273228101,
					-0.9355704541943055
				],
				[
					-15.436867882900287,
					-0.9355704541943055
				],
				[
					-15.904644187736267,
					-0.9355704541943055
				],
				[
					-16.840232486452805,
					-0.9355704541943055
				],
				[
					-17.308008791288785,
					-0.9355704541943055
				],
				[
					-18.24356140096097,
					-0.9355704541943055
				],
				[
					-18.71133770579695,
					-0.9355704541943055
				],
				[
					-19.17914969967751,
					-0.9355704541943055
				],
				[
					-19.17914969967751,
					-0.46779414935826935
				],
				[
					-19.17914969967751,
					0
				],
				[
					-20.114702309349468,
					0
				],
				[
					-20.114702309349468,
					1.4033467590303417
				],
				[
					-20.114702309349468,
					1.871123063866321
				],
				[
					-20.582478614185447,
					3.2744698228966627
				],
				[
					-20.582478614185447,
					4.210040277090968
				],
				[
					-20.582478614185447,
					5.145610731285274
				],
				[
					-21.518066912901986,
					6.548957490315615
				],
				[
					-21.518066912901986,
					8.887874703540206
				],
				[
					-21.985843217737965,
					9.823445157734511
				],
				[
					-21.985843217737965,
					12.162362370959158
				],
				[
					-22.92139582741015,
					14.501279584183749
				],
				[
					-23.38917213224613,
					17.307973102244432
				],
				[
					-23.38917213224613,
					20.114684464827292
				],
				[
					-24.32476043096267,
					23.856948437082224
				],
				[
					-24.79253673579865,
					28.53478286353146
				],
				[
					-25.728089345470835,
					32.744840985144606
				],
				[
					-25.728089345470835,
					37.4226754115939
				],
				[
					-25.728089345470835,
					41.63271568868487
				],
				[
					-25.728089345470835,
					45.37497966093986
				],
				[
					-25.728089345470835,
					50.52060823674731
				],
				[
					-25.728089345470835,
					53.32730175480799
				],
				[
					-25.260313040634628,
					56.60178942222694
				],
				[
					-24.79253673579865,
					59.40848294028751
				],
				[
					-23.85698412612669,
					61.7474001535121
				],
				[
					-23.85698412612669,
					64.08631736673681
				],
				[
					-23.85698412612669,
					66.4252345799614
				],
				[
					-23.38917213224613,
					69.23194594254426
				],
				[
					-23.38917213224613,
					70.6352927015746
				],
				[
					-23.38917213224613,
					71.57086315576885
				],
				[
					-23.38917213224613,
					73.90978036899344
				],
				[
					-23.38917213224613,
					75.78090343285987
				],
				[
					-22.453619522574172,
					77.18426803641239
				],
				[
					-21.985843217737965,
					78.58761479544273
				],
				[
					-21.985843217737965,
					79.52318524963698
				],
				[
					-21.985843217737965,
					80.92653200866732
				],
				[
					-21.985843217737965,
					82.32989661221984
				],
				[
					-21.985843217737965,
					83.26544922189203
				],
				[
					-21.518066912901986,
					84.20100183156399
				],
				[
					-21.518066912901986,
					85.13659013028052
				],
				[
					-21.518066912901986,
					85.6043664351165
				],
				[
					-21.518066912901986,
					87.00773103866914
				],
				[
					-21.518066912901986,
					88.41105995317719
				],
				[
					-21.518066912901986,
					89.8144245567297
				],
				[
					-21.518066912901986,
					91.21775347123787
				],
				[
					-21.518066912901986,
					92.62111807479039
				],
				[
					-21.518066912901986,
					94.492258983179
				],
				[
					-21.518066912901986,
					95.89558789768716
				],
				[
					-21.518066912901986,
					96.83117619640359
				],
				[
					-21.518066912901986,
					97.76672880607578
				],
				[
					-21.518066912901986,
					99.63786971446427
				],
				[
					-21.518066912901986,
					101.04123431801679
				],
				[
					-21.518066912901986,
					101.50901062285288
				],
				[
					-21.518066912901986,
					102.44456323252496
				],
				[
					-21.518066912901986,
					102.91233953736094
				],
				[
					-20.582478614185447,
					104.31570414091345
				],
				[
					-20.582478614185447,
					105.25125675058564
				],
				[
					-20.582478614185447,
					105.71906874446609
				],
				[
					-20.114702309349468,
					106.18684504930218
				],
				[
					-20.114702309349468,
					107.12239765897414
				],
				[
					-20.114702309349468,
					107.59017396381023
				],
				[
					-19.17914969967751,
					108.52576226252665
				],
				[
					-19.17914969967751,
					108.99353856736275
				],
				[
					-19.17914969967751,
					109.46131487219884
				],
				[
					-18.71133770579695,
					110.39690317091538
				],
				[
					-17.775785096124764,
					112.26800839025952
				],
				[
					-17.308008791288785,
					113.67137299381204
				],
				[
					-17.308008791288785,
					114.13914929864802
				],
				[
					-16.840232486452805,
					115.54251390220054
				],
				[
					-16.840232486452805,
					116.47806651187273
				],
				[
					-15.436867882900287,
					118.81698372509732
				],
				[
					-15.436867882900287,
					119.75257202381374
				],
				[
					-15.436867882900287,
					120.22034832864983
				],
				[
					-15.436867882900287,
					121.1559009383219
				],
				[
					-14.501315273228101,
					121.62367724315789
				],
				[
					-14.501315273228101,
					122.55926554187442
				],
				[
					-14.501315273228101,
					123.0270418467104
				],
				[
					-14.501315273228101,
					124.43040645026304
				],
				[
					-14.501315273228101,
					125.83373536477109
				],
				[
					-14.501315273228101,
					126.30151166960718
				],
				[
					-14.501315273228101,
					126.76932366348763
				],
				[
					-14.03350327934777,
					126.76932366348763
				],
				[
					-13.097950669675583,
					127.7048762731597
				],
				[
					-11.226809761287086,
					128.1726525779958
				],
				[
					-9.82348084677892,
					128.1726525779958
				],
				[
					-8.887892548062382,
					129.10824087671233
				],
				[
					-6.081199030001699,
					129.5760171815483
				],
				[
					-4.210058121613201,
					130.51156979122038
				],
				[
					-1.403364603552518,
					130.97934609605647
				],
				[
					0.4677763048359793,
					130.97934609605647
				],
				[
					1.4033289145081653,
					130.97934609605647
				],
				[
					3.2744698228966627,
					131.4471580899368
				],
				[
					4.210022432568849,
					131.4471580899368
				],
				[
					4.677834426449181,
					131.4471580899368
				],
				[
					5.14561073128516,
					131.4471580899368
				],
				[
					5.14561073128516,
					131.4471580899368
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 126,
			"versionNonce": 1268962845,
			"isDeleted": false,
			"id": "kSSNHhI114I0YMR4pYTS4",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1691.3588849160835,
			"y": 505.0402073677872,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 28.06700655869531,
			"height": 13.565726974511676,
			"seed": 67671370,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.4677763048359793,
					0
				],
				[
					0.935552609672186,
					0
				],
				[
					2.3389172132244767,
					0
				],
				[
					4.210022432568849,
					0
				],
				[
					5.613387036121367,
					-0.9355704541943055
				],
				[
					7.016751639673885,
					-1.403364603552518
				],
				[
					8.88785685901803,
					-1.403364603552518
				],
				[
					10.291221462570547,
					-2.338917213224647
				],
				[
					12.162362370959045,
					-2.8067113625828597
				],
				[
					13.56569128546721,
					-3.274487667418896
				],
				[
					15.436832193855707,
					-4.2100581216131445
				],
				[
					16.840196797408453,
					-4.6778344264492375
				],
				[
					18.243525711916618,
					-4.6778344264492375
				],
				[
					20.114666620305115,
					-5.613404880643486
				],
				[
					21.518031223857633,
					-6.0811990300017555
				],
				[
					21.985807528693613,
					-6.0811990300017555
				],
				[
					22.9213601383658,
					-6.0811990300017555
				],
				[
					23.389172132246358,
					-6.0811990300017555
				],
				[
					24.324724741918317,
					-7.016751639673828
				],
				[
					24.792501046754296,
					-7.016751639673828
				],
				[
					25.728089345470835,
					-7.016751639673828
				],
				[
					26.195865650306814,
					-7.016751639673828
				],
				[
					26.66364195514302,
					-7.016751639673828
				],
				[
					26.66364195514302,
					-7.484545789032097
				],
				[
					25.260277351590275,
					-7.484545789032097
				],
				[
					25.260277351590275,
					-7.952322093868133
				],
				[
					23.85694843708211,
					-7.952322093868133
				],
				[
					22.45358383352982,
					-8.887892548062439
				],
				[
					22.45358383352982,
					-9.355668852898475
				],
				[
					21.985807528693613,
					-9.355668852898475
				],
				[
					21.518031223857633,
					-9.355668852898475
				],
				[
					20.582442925141322,
					-9.355668852898475
				],
				[
					20.114666620305115,
					-10.29123930709278
				],
				[
					19.179114010633157,
					-10.29123930709278
				],
				[
					18.71133770579695,
					-10.759033456450993
				],
				[
					18.243525711916618,
					-10.759033456450993
				],
				[
					17.307973102244432,
					-10.759033456450993
				],
				[
					16.840196797408453,
					-10.759033456450993
				],
				[
					17.77574940708041,
					-10.759033456450993
				],
				[
					18.71133770579695,
					-10.759033456450993
				],
				[
					19.64689031546891,
					-9.823463002256688
				],
				[
					20.114666620305115,
					-9.823463002256688
				],
				[
					21.518031223857633,
					-9.355668852898475
				],
				[
					21.985807528693613,
					-8.420116243226346
				],
				[
					22.9213601383658,
					-8.420116243226346
				],
				[
					23.389172132246358,
					-8.420116243226346
				],
				[
					24.324724741918317,
					-7.952322093868133
				],
				[
					27.131418259979,
					-7.484545789032097
				],
				[
					27.59919456481498,
					-7.484545789032097
				],
				[
					27.59919456481498,
					-6.548975334837792
				],
				[
					28.06700655869531,
					-6.548975334837792
				],
				[
					28.06700655869531,
					-6.0811990300017555
				],
				[
					27.59919456481498,
					-5.145628575807507
				],
				[
					26.66364195514302,
					-4.6778344264492375
				],
				[
					26.195865650306814,
					-3.742281816777165
				],
				[
					25.260277351590275,
					-3.274487667418896
				],
				[
					24.792501046754296,
					-2.8067113625828597
				],
				[
					23.389172132246358,
					-1.403364603552518
				],
				[
					22.9213601383658,
					-0.4677941493582125
				],
				[
					21.985807528693613,
					0
				],
				[
					21.518031223857633,
					0.9355526096721292
				],
				[
					20.582442925141322,
					1.4033467590303417
				],
				[
					20.114666620305115,
					1.8711230638663778
				],
				[
					19.64689031546891,
					2.8066935180606833
				],
				[
					18.71133770579695,
					2.8066935180606833
				],
				[
					18.71133770579695,
					2.8066935180606833
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 255,
			"versionNonce": 1429399091,
			"isDeleted": false,
			"id": "r8qOaHjW",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 1714.0584944784825,
			"y": 485.8986375532647,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 127.746337890625,
			"height": 31.99663158861382,
			"seed": 125850582,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 12.798652635445528,
			"fontFamily": 1,
			"text": "Base Conditions and\nrecursive calls",
			"rawText": "Base Conditions and\nrecursive calls",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Base Conditions and\nrecursive calls",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1136,
			"versionNonce": 2021395069,
			"isDeleted": false,
			"id": "DGSoRNFcBkwQ0NzkdfvjL",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -39.16405372867064,
			"y": -1116.5844702015713,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 810.7795986610721,
			"height": 542.2523373967291,
			"seed": 1726135987,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 192,
			"versionNonce": 1694345171,
			"isDeleted": false,
			"id": "Ro7Qpx0I",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 52.988654455546225,
			"y": -1088.9323729587638,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 491.7637939453125,
			"height": 35,
			"seed": 892427965,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Leet Code questions solved till now",
			"rawText": "Leet Code questions solved till now",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Leet Code questions solved till now",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 209,
			"versionNonce": 821015261,
			"isDeleted": false,
			"id": "JKE5NDE6",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2.1683189126282514,
			"y": -959.5995579647999,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 40.17997741699219,
			"height": 125,
			"seed": 1786251357,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "# 1\n# 2\n# 3\n# 4\n# 5",
			"rawText": "# 1\n# 2\n# 3\n# 4\n# 5",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# 1\n# 2\n# 3\n# 4\n# 5",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1517,
			"versionNonce": 1564423539,
			"isDeleted": false,
			"id": "jOv7wTO62_udJtVfPB8Dz",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2006.8221005784237,
			"y": -371.9226279848217,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 810.7795986610721,
			"height": 542.2523373967291,
			"seed": 683277193,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 1505,
			"versionNonce": 26169149,
			"isDeleted": false,
			"id": "a0iCYkPB",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2340.462581710434,
			"y": -347.32856913776925,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 152.5439453125,
			"height": 35,
			"seed": 1682295665,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Merge Sort",
			"rawText": "Merge Sort",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Merge Sort",
			"lineHeight": 1.25
		},
		{
			"type": "ellipse",
			"version": 741,
			"versionNonce": 490606355,
			"isDeleted": false,
			"id": "wVvaa3loTGGUFEayld5-r",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2711.358349305736,
			"y": -344.5277569020865,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 80.9803541126721,
			"height": 75.63057892542629,
			"seed": 1166362047,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "qh6DrQAZ"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 673,
			"versionNonce": 1757175709,
			"isDeleted": false,
			"id": "qh6DrQAZ",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2744.1856499134287,
			"y": -324.45191505099,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 15.063995361328125,
			"height": 35,
			"seed": 1836332511,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "7",
			"rawText": "7",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wVvaa3loTGGUFEayld5-r",
			"originalText": "7",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 252,
			"versionNonce": 1467004083,
			"isDeleted": false,
			"id": "4ILq2TAn",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2479.7584999286505,
			"y": -238.50251214760794,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 235.67991638183594,
			"height": 25,
			"seed": 2087054449,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": " 7, 3, 2, 16, 24, 4, 11, 9",
			"rawText": " 7, 3, 2, 16, 24, 4, 11, 9",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": " 7, 3, 2, 16, 24, 4, 11, 9",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 354,
			"versionNonce": 480797693,
			"isDeleted": false,
			"id": "xYecdO9WpHuHhMPHvozv1",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2490.925155448852,
			"y": -246.36781758619787,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 256.87007981624174,
			"height": 38.53051129196288,
			"seed": 1619284593,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "_Bpa4U0rVU62pzhRnksXJ",
					"type": "arrow"
				},
				{
					"id": "x98Phg9yYrdxXVk9g7yli",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 470,
			"versionNonce": 729654867,
			"isDeleted": false,
			"id": "mwMXH5q9frZDJh85ZYwQa",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2475.2503709573075,
			"y": -185.22904100279294,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 118.60572376557957,
			"height": 28.992510253808348,
			"seed": 861595711,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 386,
			"versionNonce": 290774109,
			"isDeleted": false,
			"id": "jv2FqMPLBZe30kfVhlhju",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2643.538710545181,
			"y": -187.3375751378718,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"width": 118.60572376557957,
			"height": 28.992510253808348,
			"seed": 2134289215,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "x98Phg9yYrdxXVk9g7yli",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 533,
			"versionNonce": 3892211,
			"isDeleted": false,
			"id": "72slPVrg",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2469.3577649110093,
			"y": -182.17852886268116,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 103.27912902832031,
			"height": 23.004336306894015,
			"seed": 1660240895,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "fkEXKOr5LnPUOtjbjwhS5",
					"type": "arrow"
				},
				{
					"id": "_x5IdQuoTIGdxEHvI-g5K",
					"type": "arrow"
				},
				{
					"id": "_Bpa4U0rVU62pzhRnksXJ",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 18.403469045515212,
			"fontFamily": 1,
			"text": " 7, 3, 2, 16",
			"rawText": " 7, 3, 2, 16",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": " 7, 3, 2, 16",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 362,
			"versionNonce": 1049839805,
			"isDeleted": false,
			"id": "Ia7puK6b",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2650.936588041421,
			"y": -183.2522789400333,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 90.84687805175781,
			"height": 20.983669701365365,
			"seed": 2016183039,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "x98Phg9yYrdxXVk9g7yli",
					"type": "arrow"
				},
				{
					"id": "zXdjYU0GOcK4K_-uBmnkR",
					"type": "arrow"
				},
				{
					"id": "Lm4kKmL2qjrDWKiZo3V9h",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 16.78693576109229,
			"fontFamily": 1,
			"text": "24, 4, 11, 9",
			"rawText": "24, 4, 11, 9",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "24, 4, 11, 9",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 820,
			"versionNonce": 498101651,
			"isDeleted": false,
			"id": "h7KRh383ClOmgzHu0kHl2",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2454.2808499088424,
			"y": -132.41661654149112,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 64.63624212194279,
			"height": 35,
			"seed": 1861247455,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "cdSvUd8Y"
				},
				{
					"id": "xMYOf7F1ElXObwcDavWYB",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 165,
			"versionNonce": 637872413,
			"isDeleted": false,
			"id": "cdSvUd8Y",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2466.838976462978,
			"y": -127.41661654149112,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 39.519989013671875,
			"height": 25,
			"seed": 959755519,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "7, 3",
			"rawText": "7, 3",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "h7KRh383ClOmgzHu0kHl2",
			"originalText": "7, 3",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 881,
			"versionNonce": 118702899,
			"isDeleted": false,
			"id": "x5Hq2gwPhk6nBr1wgMetK",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2539.646921990095,
			"y": -132.89276701604683,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"width": 64.22728489059224,
			"height": 35,
			"seed": 1047767729,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "elbz5VuB"
				},
				{
					"id": "_x5IdQuoTIGdxEHvI-g5K",
					"type": "arrow"
				},
				{
					"id": "IZXSqYuaPQEkaUiEbvMss",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 169,
			"versionNonce": 421264765,
			"isDeleted": false,
			"id": "elbz5VuB",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2547.9605766424224,
			"y": -127.89276701604683,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 47.5999755859375,
			"height": 25,
			"seed": 247427057,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "2, 16",
			"rawText": "2, 16",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "x5Hq2gwPhk6nBr1wgMetK",
			"originalText": "2, 16",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1036,
			"versionNonce": 348808403,
			"isDeleted": false,
			"id": "CcKq6L74MqNVObo2Idtqi",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2630.3236649324754,
			"y": -131.47974929818628,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 70.22741237260556,
			"height": 35,
			"seed": 531062641,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "Uy87kZSf"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 386,
			"versionNonce": 1058620893,
			"isDeleted": false,
			"id": "Uy87kZSf",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2637.9473885137977,
			"y": -126.47974929818628,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 54.97996520996094,
			"height": 25,
			"seed": 1598835025,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "24, 4",
			"rawText": "24, 4",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CcKq6L74MqNVObo2Idtqi",
			"originalText": "24, 4",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 948,
			"versionNonce": 1315721843,
			"isDeleted": false,
			"id": "drrLFEONVuJkChYmBhR-4",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2717.3204868571615,
			"y": -131.3445592234891,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"width": 64.22728489059224,
			"height": 35,
			"seed": 309917489,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "pNbB4b8r"
				},
				{
					"id": "Lm4kKmL2qjrDWKiZo3V9h",
					"type": "arrow"
				},
				{
					"id": "hReZW5lAizf_0a_ZjsPnD",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 242,
			"versionNonce": 1527677501,
			"isDeleted": false,
			"id": "pNbB4b8r",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2730.3541351007975,
			"y": -126.34455922348911,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 38.15998840332031,
			"height": 25,
			"seed": 2073356561,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "11, 9",
			"rawText": "11, 9",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "drrLFEONVuJkChYmBhR-4",
			"originalText": "11, 9",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 952,
			"versionNonce": 79662099,
			"isDeleted": false,
			"id": "BXDqBPTqvHgj8YclJIrkQ",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2438.6746258190024,
			"y": -81.23106369079328,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 33.63953324528618,
			"height": 35,
			"seed": 862210815,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "Ycn4qRLV"
				},
				{
					"id": "jC0xTpdcKVwXhI1JzlTZL",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 300,
			"versionNonce": 1373450909,
			"isDeleted": false,
			"id": "Ycn4qRLV",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2450.1143951882273,
			"y": -76.23106369079328,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 10.759994506835938,
			"height": 25,
			"seed": 1807782687,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "7",
			"rawText": "7",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BXDqBPTqvHgj8YclJIrkQ",
			"originalText": "7",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 988,
			"versionNonce": 733647283,
			"isDeleted": false,
			"id": "DvreBiuTRhVhu3B1gFbcr",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2488.317816027542,
			"y": -80.415390732711,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"width": 30.201974755925217,
			"height": 35,
			"seed": 1033819967,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "vXrF2yaA"
				},
				{
					"id": "xMYOf7F1ElXObwcDavWYB",
					"type": "arrow"
				},
				{
					"id": "GEdVxYM8yoqsF-30OG8tP",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 278,
			"versionNonce": 1882642173,
			"isDeleted": false,
			"id": "vXrF2yaA",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2496.608805846911,
			"y": -75.415390732711,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 13.6199951171875,
			"height": 25,
			"seed": 526358367,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "3",
			"rawText": "3",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "DvreBiuTRhVhu3B1gFbcr",
			"originalText": "3",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 987,
			"versionNonce": 1954800467,
			"isDeleted": false,
			"id": "VKjLSepNx-bNLoEPMRNaF",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2534.5643003977066,
			"y": -80.7599758416391,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 33.63953324528618,
			"height": 35,
			"seed": 2028106015,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "b3OeVAYl"
				},
				{
					"id": "btHTJKvvMh8iRNdD428NM",
					"type": "arrow"
				},
				{
					"id": "T55HYBQru-kI7aNCtbK7O",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 337,
			"versionNonce": 1889333085,
			"isDeleted": false,
			"id": "b3OeVAYl",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2544.264071903162,
			"y": -75.7599758416391,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 14.239990234375,
			"height": 25,
			"seed": 1188361535,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "2",
			"rawText": "2",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VKjLSepNx-bNLoEPMRNaF",
			"originalText": "2",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1020,
			"versionNonce": 661782771,
			"isDeleted": false,
			"id": "iRNOw46V8M-czQXFSv3UA",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2584.2074906062467,
			"y": -79.94430288355683,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"width": 30.201974755925217,
			"height": 35,
			"seed": 404878687,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "g8KTCoJ1"
				},
				{
					"id": "YxjYOSW6ubUw3UdQcTZr0",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 314,
			"versionNonce": 1096874941,
			"isDeleted": false,
			"id": "g8KTCoJ1",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2590.1984850032522,
			"y": -74.94430288355683,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 18.219985961914062,
			"height": 25,
			"seed": 337244543,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "16",
			"rawText": "16",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "iRNOw46V8M-czQXFSv3UA",
			"originalText": "16",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1090,
			"versionNonce": 1040935571,
			"isDeleted": false,
			"id": "oSjzESvTP4or5MQ59vSo2",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2627.1183692301565,
			"y": -79.59720711747597,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 37.75529429211881,
			"height": 35,
			"seed": 413712351,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "SRAiTKTK"
				},
				{
					"id": "vClkp1UxwuE4wF8GaXE-E",
					"type": "arrow"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 441,
			"versionNonce": 178551837,
			"isDeleted": false,
			"id": "SRAiTKTK",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2632.476027362544,
			"y": -74.59720711747597,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 27.03997802734375,
			"height": 25,
			"seed": 509832191,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158216,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "24",
			"rawText": "24",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "oSjzESvTP4or5MQ59vSo2",
			"originalText": "24",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1044,
			"versionNonce": 1023844403,
			"isDeleted": false,
			"id": "M-kN6hubCnOHj08uIuw9M",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2676.50432805305,
			"y": -78.7815341593937,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"width": 30.201974755925217,
			"height": 35,
			"seed": 1278448671,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "TXchz12K"
				}
			],
			"updated": 1715421158216,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 338,
			"versionNonce": 1951985789,
			"isDeleted": false,
			"id": "TXchz12K",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2685.205321534528,
			"y": -73.7815341593937,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 12.79998779296875,
			"height": 25,
			"seed": 2047457343,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "4",
			"rawText": "4",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "M-kN6hubCnOHj08uIuw9M",
			"originalText": "4",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1011,
			"versionNonce": 1313481171,
			"isDeleted": false,
			"id": "M17Iw2Jv8SLyW-xWL7SD5",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2719.6100669245225,
			"y": -78.03891420392902,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 33.63953324528618,
			"height": 35,
			"seed": 567125105,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "IutFOYDx"
				},
				{
					"id": "RYzNC4t0yOULj3A-oFpWz",
					"type": "arrow"
				}
			],
			"updated": 1715421158217,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 363,
			"versionNonce": 742381789,
			"isDeleted": false,
			"id": "IutFOYDx",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2731.00983537822,
			"y": -73.03891420392902,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 10.839996337890625,
			"height": 25,
			"seed": 778169937,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "11",
			"rawText": "11",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "M17Iw2Jv8SLyW-xWL7SD5",
			"originalText": "11",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1048,
			"versionNonce": 451702643,
			"isDeleted": false,
			"id": "NKk4Mpn21_a6AiOUVzG7y",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2763.0153914906164,
			"y": -79.72627354053223,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"width": 30.201974755925217,
			"height": 35,
			"seed": 428997681,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "FiQNYPt9"
				},
				{
					"id": "L19_Y-rN7QMOAFB46iI0Y",
					"type": "arrow"
				}
			],
			"updated": 1715421158217,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 342,
			"versionNonce": 736802109,
			"isDeleted": false,
			"id": "FiQNYPt9",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2772.0263825306884,
			"y": -74.72627354053223,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 12.17999267578125,
			"height": 25,
			"seed": 591744529,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "9",
			"rawText": "9",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NKk4Mpn21_a6AiOUVzG7y",
			"originalText": "9",
			"lineHeight": 1.25
		},
		{
			"type": "arrow",
			"version": 270,
			"versionNonce": 1697909011,
			"isDeleted": false,
			"id": "_Bpa4U0rVU62pzhRnksXJ",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2565.767972240298,
			"y": -206.39499326774896,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 10.262893660537884,
			"height": 20.444947007494022,
			"seed": 901812721,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "xYecdO9WpHuHhMPHvozv1",
				"focus": 0.31278565635167976,
				"gap": 1.4423130264860475
			},
			"endBinding": {
				"elementId": "72slPVrg",
				"focus": 0.2797613356804149,
				"gap": 3.771517397573774
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-10.262893660537884,
					20.444947007494022
				]
			]
		},
		{
			"type": "arrow",
			"version": 349,
			"versionNonce": 1052444061,
			"isDeleted": false,
			"id": "x98Phg9yYrdxXVk9g7yli",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2660.6170125806266,
			"y": -205.57417549607794,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 11.514316391473585,
			"height": 16.677853988950744,
			"seed": 1143818993,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "xYecdO9WpHuHhMPHvozv1",
				"focus": -0.18621784901728383,
				"gap": 2.2631307981570643
			},
			"endBinding": {
				"elementId": "Ia7puK6b",
				"focus": -0.36121625245084266,
				"gap": 5.6440425670938765
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					11.514316391473585,
					16.677853988950744
				]
			]
		},
		{
			"type": "arrow",
			"version": 200,
			"versionNonce": 1654091443,
			"isDeleted": false,
			"id": "fkEXKOr5LnPUOtjbjwhS5",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2528.4952218695666,
			"y": -156.06056793218062,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 27.475501014910606,
			"height": 25.147101845853427,
			"seed": 664858129,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "72slPVrg",
				"focus": -0.19761657955147496,
				"gap": 3.1136246236065404
			},
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-27.475501014910606,
					25.147101845853427
				]
			]
		},
		{
			"type": "arrow",
			"version": 306,
			"versionNonce": 1174089469,
			"isDeleted": false,
			"id": "_x5IdQuoTIGdxEHvI-g5K",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2538.370802419352,
			"y": -156.06056793218062,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 30.64242823937002,
			"height": 22.167800916133785,
			"seed": 208636177,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424375,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "72slPVrg",
				"gap": 3.1136246236065404,
				"focus": 0.04189962060394819
			},
			"endBinding": {
				"elementId": "x5Hq2gwPhk6nBr1wgMetK",
				"gap": 1,
				"focus": 0.40539209571157353
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					30.64242823937002,
					22.167800916133785
				]
			]
		},
		{
			"type": "arrow",
			"version": 205,
			"versionNonce": 1438457939,
			"isDeleted": false,
			"id": "zXdjYU0GOcK4K_-uBmnkR",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2690.088611238727,
			"y": -158.85468246414345,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 17.6961179175878,
			"height": 28.8725938099862,
			"seed": 1617727793,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Ia7puK6b",
				"focus": 0.07104812819261715,
				"gap": 3.413926774524512
			},
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-17.6961179175878,
					28.8725938099862
				]
			]
		},
		{
			"type": "arrow",
			"version": 304,
			"versionNonce": 430429213,
			"isDeleted": false,
			"id": "Lm4kKmL2qjrDWKiZo3V9h",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2715.1576770560423,
			"y": -157.9233050319735,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 26.858718505116485,
			"height": 24.21572441368349,
			"seed": 1204211089,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424375,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Ia7puK6b",
				"gap": 4.3453042066944505,
				"focus": -0.04102899409823072
			},
			"endBinding": {
				"elementId": "drrLFEONVuJkChYmBhR-4",
				"gap": 2.36302139480091,
				"focus": 0.2836213945338186
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					26.858718505116485,
					24.21572441368349
				]
			]
		},
		{
			"type": "arrow",
			"version": 221,
			"versionNonce": 609038557,
			"isDeleted": false,
			"id": "jC0xTpdcKVwXhI1JzlTZL",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2481.4608480727284,
			"y": -98.78106014601968,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 17.23040255468277,
			"height": 13.504910590549684,
			"seed": 654796209,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424375,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "BXDqBPTqvHgj8YclJIrkQ",
				"gap": 4.045085864676722,
				"focus": -0.4790235558347137
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-17.23040255468277,
					13.504910590549684
				]
			]
		},
		{
			"type": "arrow",
			"version": 337,
			"versionNonce": 1699896733,
			"isDeleted": false,
			"id": "xMYOf7F1ElXObwcDavWYB",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2497.100609096298,
			"y": -96.41661654149112,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 3.919111758357303,
			"height": 13.934599282530911,
			"seed": 442000081,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424375,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "h7KRh383ClOmgzHu0kHl2",
				"gap": 1,
				"focus": -0.14227994322369084
			},
			"endBinding": {
				"elementId": "DvreBiuTRhVhu3B1gFbcr",
				"gap": 2.0666265262491947,
				"focus": 0.1550246916451123
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					3.919111758357303,
					13.934599282530911
				]
			]
		},
		{
			"type": "arrow",
			"version": 212,
			"versionNonce": 834799293,
			"isDeleted": false,
			"id": "btHTJKvvMh8iRNdD428NM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2558.7648729455345,
			"y": -99.24675774437813,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 6.519588731548993,
			"height": 17.230420319229438,
			"seed": 1108438609,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424376,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "VKjLSepNx-bNLoEPMRNaF",
				"gap": 1.2563615835095874,
				"focus": -0.2660149672148787
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-6.519588731548993,
					17.230420319229438
				]
			]
		},
		{
			"type": "arrow",
			"version": 196,
			"versionNonce": 1008093021,
			"isDeleted": false,
			"id": "IZXSqYuaPQEkaUiEbvMss",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2585.112379519829,
			"y": -96.89276701604683,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 10.441768762315405,
			"height": 19.06761915338936,
			"seed": 1436654225,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424375,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "x5Hq2gwPhk6nBr1wgMetK",
				"gap": 1,
				"focus": -0.07724508204372084
			},
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					10.441768762315405,
					19.06761915338936
				]
			]
		},
		{
			"type": "arrow",
			"version": 193,
			"versionNonce": 1947008307,
			"isDeleted": false,
			"id": "lO4Ea9QVws9hXLOwJNUkx",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2649.5534650723785,
			"y": -75.25357226276165,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 0.020361101058824715,
			"height": 3.037273198254262,
			"seed": 1084413649,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					0.020361101058824715,
					-3.037273198254262
				]
			]
		},
		{
			"type": "arrow",
			"version": 147,
			"versionNonce": 1563616125,
			"isDeleted": false,
			"id": "pI6a4psRiYRbxQHWjLt2m",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2674.255248185479,
			"y": -100.17813517654807,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 15.833363053247922,
			"height": 21.887289715532148,
			"seed": 1916563761,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					15.833363053247922,
					21.887289715532148
				]
			]
		},
		{
			"type": "arrow",
			"version": 210,
			"versionNonce": 2033272957,
			"isDeleted": false,
			"id": "hReZW5lAizf_0a_ZjsPnD",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2738.0057856595417,
			"y": -95.34455922348913,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 5.073990186467199,
			"height": 18.45077102845464,
			"seed": 369716273,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424375,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "drrLFEONVuJkChYmBhR-4",
				"gap": 1,
				"focus": 0.17171603663277316
			},
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-5.073990186467199,
					18.45077102845464
				]
			]
		},
		{
			"type": "arrow",
			"version": 227,
			"versionNonce": 225275229,
			"isDeleted": false,
			"id": "L19_Y-rN7QMOAFB46iI0Y",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2766.4612409148167,
			"y": -99.71243757818962,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 13.561543277699002,
			"height": 18.98616403765739,
			"seed": 1594738865,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424376,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "NKk4Mpn21_a6AiOUVzG7y",
				"gap": 1,
				"focus": 0.5478314842397981
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					13.561543277699002,
					18.98616403765739
				]
			]
		},
		{
			"type": "rectangle",
			"version": 686,
			"versionNonce": 2143259763,
			"isDeleted": false,
			"id": "xlz6HgrY9RfD_eePzmvQe",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2455.474001285954,
			"y": -27.066831573468363,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 50.76174858183913,
			"height": 35,
			"seed": 2102532799,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "rDk0XVXv"
				},
				{
					"id": "-KqWohyAxLklTlPcZQ37q",
					"type": "arrow"
				},
				{
					"id": "GEdVxYM8yoqsF-30OG8tP",
					"type": "arrow"
				},
				{
					"id": "p5zA3rSzAff8H9bupPJhs",
					"type": "arrow"
				}
			],
			"updated": 1715421158217,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 170,
			"versionNonce": 119793725,
			"isDeleted": false,
			"id": "rDk0XVXv",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2461.0948810700374,
			"y": -22.066831573468363,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 39.519989013671875,
			"height": 25,
			"seed": 2118951775,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "3, 7",
			"rawText": "3, 7",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xlz6HgrY9RfD_eePzmvQe",
			"originalText": "3, 7",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 956,
			"versionNonce": 1536919059,
			"isDeleted": false,
			"id": "KkkoOtgjv0zq6IPdT5ZQG",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2534.2014860595705,
			"y": -24.12303711892939,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"width": 64.22728489059224,
			"height": 35,
			"seed": 350503135,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "4uRDHRrY"
				},
				{
					"id": "T55HYBQru-kI7aNCtbK7O",
					"type": "arrow"
				}
			],
			"updated": 1715421158217,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 242,
			"versionNonce": 1649793181,
			"isDeleted": false,
			"id": "4uRDHRrY",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2542.515140711898,
			"y": -19.12303711892939,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 47.5999755859375,
			"height": 25,
			"seed": 1770441983,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "2, 16",
			"rawText": "2, 16",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KkkoOtgjv0zq6IPdT5ZQG",
			"originalText": "2, 16",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 804,
			"versionNonce": 2030521267,
			"isDeleted": false,
			"id": "uzabB5fxmpKNrj-g8onNp",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2632.5116285444356,
			"y": -22.070888408155156,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 66.83694392647112,
			"height": 35,
			"seed": 582355921,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "ywbtldX4"
				},
				{
					"id": "HmwXeeO23WBQ2lmZ65mLy",
					"type": "arrow"
				},
				{
					"id": "ne_tSNxZ8-px2d1-oL53u",
					"type": "arrow"
				}
			],
			"updated": 1715421158217,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 297,
			"versionNonce": 1990900989,
			"isDeleted": false,
			"id": "ywbtldX4",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2638.440117902691,
			"y": -17.070888408155156,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 54.97996520996094,
			"height": 25,
			"seed": 2022074801,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "4, 24",
			"rawText": "4, 24",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uzabB5fxmpKNrj-g8onNp",
			"originalText": "4, 24",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1047,
			"versionNonce": 740908371,
			"isDeleted": false,
			"id": "1eaB1Royh4Sc8dc5w6ZOF",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2722.1445991086803,
			"y": -20.61726893684323,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"width": 64.22728489059224,
			"height": 35,
			"seed": 908343825,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "v0KhnzWs"
				},
				{
					"id": "RYzNC4t0yOULj3A-oFpWz",
					"type": "arrow"
				},
				{
					"id": "Rudfahc4i3SwxWcDZkuC_",
					"type": "arrow"
				},
				{
					"id": "IpTR6juc9WKRNWqw09dXk",
					"type": "arrow"
				}
			],
			"updated": 1715421158217,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 343,
			"versionNonce": 195302749,
			"isDeleted": false,
			"id": "v0KhnzWs",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2735.1782473523162,
			"y": -15.617268936843232,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 38.15998840332031,
			"height": 25,
			"seed": 1385484273,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "9, 11",
			"rawText": "9, 11",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "1eaB1Royh4Sc8dc5w6ZOF",
			"originalText": "9, 11",
			"lineHeight": 1.25
		},
		{
			"type": "arrow",
			"version": 194,
			"versionNonce": 728873405,
			"isDeleted": false,
			"id": "-KqWohyAxLklTlPcZQ37q",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2464.990028227335,
			"y": -47.58060407972624,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 12.654938795179532,
			"height": 19.49545189408485,
			"seed": 643833087,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424377,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "xlz6HgrY9RfD_eePzmvQe",
				"gap": 1.018320612173028,
				"focus": 0.23981022025760015
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					12.654938795179532,
					19.49545189408485
				]
			]
		},
		{
			"type": "arrow",
			"version": 287,
			"versionNonce": 1137847933,
			"isDeleted": false,
			"id": "GEdVxYM8yoqsF-30OG8tP",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2500.292321746606,
			"y": -44.415390732711,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 12.386585075733365,
			"height": 15.646197674973745,
			"seed": 1578637841,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424377,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "DvreBiuTRhVhu3B1gFbcr",
				"gap": 1,
				"focus": -0.3978345424829849
			},
			"endBinding": {
				"elementId": "xlz6HgrY9RfD_eePzmvQe",
				"gap": 1.7023614842688914,
				"focus": -0.20774848378704225
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-12.386585075733365,
					15.646197674973745
				]
			]
		},
		{
			"type": "arrow",
			"version": 287,
			"versionNonce": 1238140925,
			"isDeleted": false,
			"id": "T55HYBQru-kI7aNCtbK7O",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2554.647173483001,
			"y": -44.759975841639104,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 10.800319418695835,
			"height": 19.636938722709715,
			"seed": 422101905,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424377,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "VKjLSepNx-bNLoEPMRNaF",
				"gap": 1,
				"focus": 0.2613710247269857
			},
			"endBinding": {
				"elementId": "KkkoOtgjv0zq6IPdT5ZQG",
				"gap": 1,
				"focus": 0.22299160135026844
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					10.800319418695835,
					19.636938722709715
				]
			]
		},
		{
			"type": "arrow",
			"version": 198,
			"versionNonce": 2123940829,
			"isDeleted": false,
			"id": "YxjYOSW6ubUw3UdQcTZr0",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2598.193011506827,
			"y": -43.94430288355683,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 19.650476275462097,
			"height": 20.30549464999838,
			"seed": 747613457,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424376,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "iRNOw46V8M-czQXFSv3UA",
				"gap": 1,
				"focus": -0.5240202045850202
			},
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-19.650476275462097,
					20.30549464999838
				]
			]
		},
		{
			"type": "arrow",
			"version": 176,
			"versionNonce": 971915325,
			"isDeleted": false,
			"id": "vClkp1UxwuE4wF8GaXE-E",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2652.3932121034823,
			"y": -43.597207117475975,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 17.470188654957383,
			"height": 24.062696305465934,
			"seed": 1742068849,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424376,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "oSjzESvTP4or5MQ59vSo2",
				"gap": 1,
				"focus": 0.22272393813493768
			},
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					17.470188654957383,
					24.062696305465934
				]
			]
		},
		{
			"type": "arrow",
			"version": 196,
			"versionNonce": 1314160733,
			"isDeleted": false,
			"id": "HmwXeeO23WBQ2lmZ65mLy",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2691.068980927251,
			"y": -45.52845536895205,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 15.753794636648308,
			"height": 22.457566960796896,
			"seed": 803295889,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424377,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "uzabB5fxmpKNrj-g8onNp",
				"gap": 1,
				"focus": -0.07862003013669518
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-15.753794636648308,
					22.457566960796896
				]
			]
		},
		{
			"type": "arrow",
			"version": 282,
			"versionNonce": 1359880573,
			"isDeleted": false,
			"id": "RYzNC4t0yOULj3A-oFpWz",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2730.483370954741,
			"y": -42.038914203929025,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 22.834268734751276,
			"height": 19.426193373001,
			"seed": 921774641,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424377,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "M17Iw2Jv8SLyW-xWL7SD5",
				"gap": 1,
				"focus": 0.7406288137024023
			},
			"endBinding": {
				"elementId": "1eaB1Royh4Sc8dc5w6ZOF",
				"gap": 1.9954518940847947,
				"focus": 0.4171126465011946
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					22.834268734751276,
					19.426193373001
				]
			]
		},
		{
			"type": "arrow",
			"version": 187,
			"versionNonce": 2099702237,
			"isDeleted": false,
			"id": "Rudfahc4i3SwxWcDZkuC_",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2769.734881564659,
			"y": -45.18642188566082,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 11.286612723701182,
			"height": 23.56915294881759,
			"seed": 1059555025,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424377,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "1eaB1Royh4Sc8dc5w6ZOF",
				"gap": 1,
				"focus": -0.11530398767134713
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-11.286612723701182,
					23.56915294881759
				]
			]
		},
		{
			"type": "rectangle",
			"version": 599,
			"versionNonce": 971352435,
			"isDeleted": false,
			"id": "8nLDmEASSVoxHmeci1cef",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2461.192936167818,
			"y": 29.929373620467572,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 118.60572376557957,
			"height": 35,
			"seed": 285001791,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "mClnaHph"
				},
				{
					"id": "p5zA3rSzAff8H9bupPJhs",
					"type": "arrow"
				}
			],
			"updated": 1715421158217,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 147,
			"versionNonce": 2142903101,
			"isDeleted": false,
			"id": "mClnaHph",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2469.365816055979,
			"y": 34.92937362046757,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"width": 102.25996398925781,
			"height": 25,
			"seed": 630049169,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "2, 3, 7, 16",
			"rawText": "2, 3, 7, 16",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8nLDmEASSVoxHmeci1cef",
			"originalText": "2, 3, 7, 16",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 495,
			"versionNonce": 83231507,
			"isDeleted": false,
			"id": "_6orfvQ6X5AULFUmC-W8K",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2645.1561660256707,
			"y": 31.934533177898942,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"width": 118.60572376557957,
			"height": 35,
			"seed": 981992255,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "WZtS9Lwe"
				}
			],
			"updated": 1715421158217,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 120,
			"versionNonce": 1873652637,
			"isDeleted": false,
			"id": "WZtS9Lwe",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2650.3190514069956,
			"y": 36.93453317789894,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 108.27995300292969,
			"height": 25,
			"seed": 1286295103,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "4, 9, 11, 24",
			"rawText": "4, 9, 11, 24",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "_6orfvQ6X5AULFUmC-W8K",
			"originalText": "4, 9, 11, 24",
			"lineHeight": 1.25
		},
		{
			"type": "arrow",
			"version": 420,
			"versionNonce": 1542912765,
			"isDeleted": false,
			"id": "p5zA3rSzAff8H9bupPJhs",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2482.3397582302487,
			"y": 9.303179016671493,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 31.63904350619032,
			"height": 19.18272417196809,
			"seed": 1463896799,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424377,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "xlz6HgrY9RfD_eePzmvQe",
				"gap": 1.3700105901398558,
				"focus": 0.5463849448478938
			},
			"endBinding": {
				"elementId": "8nLDmEASSVoxHmeci1cef",
				"gap": 1.4434704318279898,
				"focus": 0.28046290878573943
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					31.63904350619032,
					19.18272417196809
				]
			]
		},
		{
			"type": "arrow",
			"version": 127,
			"versionNonce": 1334849533,
			"isDeleted": false,
			"id": "8qBcxtPFareYTvS-BR4zf",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2553.8390236059495,
			"y": 9.303179016671493,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 24.912638668444288,
			"height": 21.424865453495045,
			"seed": 41669567,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-24.912638668444288,
					21.424865453495045
				]
			]
		},
		{
			"type": "arrow",
			"version": 175,
			"versionNonce": 67005629,
			"isDeleted": false,
			"id": "ne_tSNxZ8-px2d1-oL53u",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2660.714247294942,
			"y": 14.783951920995268,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 22.919619972234614,
			"height": 18.435356416015704,
			"seed": 894106751,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424377,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "uzabB5fxmpKNrj-g8onNp",
				"gap": 1.85484032915042,
				"focus": 0.5306479306358738
			},
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					22.919619972234614,
					18.435356416015704
				]
			]
		},
		{
			"type": "arrow",
			"version": 189,
			"versionNonce": 1338484285,
			"isDeleted": false,
			"id": "IpTR6juc9WKRNWqw09dXk",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2745.268527742919,
			"y": 15.382731063156768,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 24.763947643710708,
			"height": 18.334822444489106,
			"seed": 1077297279,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424377,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "1eaB1Royh4Sc8dc5w6ZOF",
				"gap": 1,
				"focus": -0.2869474559949569
			},
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-24.763947643710708,
					18.334822444489106
				]
			]
		},
		{
			"type": "rectangle",
			"version": 412,
			"versionNonce": 738711539,
			"isDeleted": false,
			"id": "7ptBVJfAuuyalumR4O_YB",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2490.868022604793,
			"y": 85.91888144205711,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 256.87007981624174,
			"height": 38.53051129196288,
			"seed": 600033887,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "NwbVqlrk"
				},
				{
					"id": "DifMGu9WoxPlvqq0lIaiQ",
					"type": "arrow"
				},
				{
					"id": "ykuwZkTJsH52s5Zc4mUKk",
					"type": "arrow"
				}
			],
			"updated": 1715421158217,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 154,
			"versionNonce": 1526207677,
			"isDeleted": false,
			"id": "NwbVqlrk",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2523.1430969977773,
			"y": 92.68413708803855,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 192.31993103027344,
			"height": 25,
			"seed": 445259103,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "2, 3, 4, 7, 9, 11, 24",
			"rawText": "2, 3, 4, 7, 9, 11, 24",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7ptBVJfAuuyalumR4O_YB",
			"originalText": "2, 3, 4, 7, 9, 11, 24",
			"lineHeight": 1.25
		},
		{
			"type": "arrow",
			"version": 195,
			"versionNonce": 951620445,
			"isDeleted": false,
			"id": "DifMGu9WoxPlvqq0lIaiQ",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2547.7292720067203,
			"y": 64.42285661644826,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 42.20689484736886,
			"height": 18.75859674193009,
			"seed": 1898703025,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424378,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "7ptBVJfAuuyalumR4O_YB",
				"gap": 2.737428083678765,
				"focus": 0.11723704151794587
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					42.20689484736886,
					18.75859674193009
				]
			]
		},
		{
			"type": "arrow",
			"version": 188,
			"versionNonce": 1315446717,
			"isDeleted": false,
			"id": "ykuwZkTJsH52s5Zc4mUKk",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2683.7292698277997,
			"y": 66.76767748218765,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 23.05749959715149,
			"height": 17.976999725355256,
			"seed": 372015665,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421424378,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "7ptBVJfAuuyalumR4O_YB",
				"gap": 1.1742042345142067,
				"focus": 0.09894441308301144
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-23.05749959715149,
					17.976999725355256
				]
			]
		},
		{
			"type": "rectangle",
			"version": 271,
			"versionNonce": 1498593075,
			"isDeleted": false,
			"id": "TWagkbDecuwdy3_KJ9qwp",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2425.3845077026426,
			"y": -255.47507445589684,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 375.4903255108279,
			"height": 393.33935415652655,
			"seed": 324371249,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158217,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 360,
			"versionNonce": 599640445,
			"isDeleted": false,
			"id": "ndV7AkyU",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2031.4061999610171,
			"y": -288.9081605860449,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 369.14056396484375,
			"height": 92.01810556629403,
			"seed": 76110097,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"fontSize": 18.403621113258804,
			"fontFamily": 1,
			"text": "Steps : \n(1) Divide away into parts\n(2) Get both parts sorted via recursion\n(3) Merge the sorted parts",
			"rawText": "Steps : \n(1) Divide away into parts\n(2) Get both parts sorted via recursion\n(3) Merge the sorted parts",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Steps : \n(1) Divide away into parts\n(2) Get both parts sorted via recursion\n(3) Merge the sorted parts",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1633,
			"versionNonce": 1459312851,
			"isDeleted": false,
			"id": "iSKSP0Ei",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2043.010318866266,
			"y": -178.56839612391116,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 216.37985229492188,
			"height": 25,
			"seed": 29096991,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Explanation point 3 : ",
			"rawText": "Explanation point 3 : ",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Explanation point 3 : ",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1662,
			"versionNonce": 732008925,
			"isDeleted": false,
			"id": "4tsQygCN",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2107.1864938608965,
			"y": -112.50281794155202,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 190.3799285888672,
			"height": 25,
			"seed": 2126151967,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "arr1 = [2, 3, 7, 16]",
			"rawText": "arr1 = [2, 3, 7, 16]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "arr1 = [2, 3, 7, 16]",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 1814,
			"versionNonce": 106874483,
			"isDeleted": false,
			"id": "hzJp4Por",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2105.546170751039,
			"y": -54.439998838408286,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 205.21990966796875,
			"height": 25,
			"seed": 1593355153,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "arr2 = [4, 9, 11, 24]",
			"rawText": "arr2 = [4, 9, 11, 24]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "arr2 = [4, 9, 11, 24]",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 421,
			"versionNonce": 682446397,
			"isDeleted": false,
			"id": "ELEWsBMc",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2069.8537108330593,
			"y": -14.075245860839686,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 340.3095703125,
			"height": 20.937775057453845,
			"seed": 967315761,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"fontSize": 16.750220045963076,
			"fontFamily": 1,
			"text": "Sorted Array = [2, 3, 4, 7, 9, 11, 16, 24]",
			"rawText": "Sorted Array = [2, 3, 4, 7, 9, 11, 16, 24]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Sorted Array = [2, 3, 4, 7, 9, 11, 16, 24]",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 156,
			"versionNonce": 2118352915,
			"isDeleted": false,
			"id": "54UWnQCVvfwmlrGVOXQye",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2192.2137053430756,
			"y": -130.08086812059537,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.0706990740150104,
			"height": 10.349977594611744,
			"seed": 544059921,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.7137948445087403
				],
				[
					0,
					1.070685459510969
				],
				[
					0,
					1.7844803040197093
				],
				[
					0,
					2.141370919021938
				],
				[
					0.7138084590128528,
					2.4982751485284496
				],
				[
					0.7138084590128528,
					3.212056378532907
				],
				[
					0.7138084590128528,
					3.5689606080394185
				],
				[
					0.7138084590128528,
					4.639646067550387
				],
				[
					1.0706990740150104,
					5.353440912059128
				],
				[
					1.0706990740150104,
					5.710331527061356
				],
				[
					1.0706990740150104,
					6.067235756567868
				],
				[
					1.0706990740150104,
					6.781016986572325
				],
				[
					1.0706990740150104,
					7.137921216078837
				],
				[
					1.0706990740150104,
					7.851716060587577
				],
				[
					1.0706990740150104,
					8.208606675589806
				],
				[
					1.0706990740150104,
					8.565497290592035
				],
				[
					1.0706990740150104,
					9.279292135100775
				],
				[
					1.0706990740150104,
					9.636196364607287
				],
				[
					1.0706990740150104,
					10.349977594611744
				],
				[
					1.0706990740150104,
					10.349977594611744
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 160,
			"versionNonce": 432176797,
			"isDeleted": false,
			"id": "bLtJtxRC-1vEQztQnA4a1",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2188.287854120034,
			"y": -121.51537083000332,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 9.279292135100604,
			"height": 3.5689606080394185,
			"seed": 848949073,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3568906150021576,
					0
				],
				[
					1.0706990740150104,
					0
				],
				[
					1.0706990740150104,
					0.7137948445087403
				],
				[
					1.427589689017168,
					1.070699074015252
				],
				[
					1.427589689017168,
					1.7844803040197093
				],
				[
					2.141370919021938,
					1.7844803040197093
				],
				[
					2.141370919021938,
					2.141384533526221
				],
				[
					2.498288763032633,
					2.8551793780349612
				],
				[
					3.2120699930369483,
					3.21206999303719
				],
				[
					3.2120699930369483,
					3.5689606080394185
				],
				[
					3.568960608039106,
					3.5689606080394185
				],
				[
					3.925851223041718,
					3.5689606080394185
				],
				[
					4.639659682054571,
					3.5689606080394185
				],
				[
					4.996550297056729,
					3.5689606080394185
				],
				[
					5.710331527061044,
					3.21206999303719
				],
				[
					6.067249371072194,
					2.4982751485284496
				],
				[
					6.781030601076509,
					2.4982751485284496
				],
				[
					7.1379212160786665,
					2.141384533526221
				],
				[
					7.494811831080824,
					1.4275896890174806
				],
				[
					8.208620290094132,
					1.070699074015252
				],
				[
					8.56551090509629,
					1.070699074015252
				],
				[
					8.56551090509629,
					0.3569042295065117
				],
				[
					9.279292135100604,
					0.3569042295065117
				],
				[
					9.279292135100604,
					0.3569042295065117
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 189,
			"versionNonce": 950011315,
			"isDeleted": false,
			"id": "R6mNiPz5ezbV3nxwdQEFe",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2200.065407789158,
			"y": -69.76541478442317,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 0,
			"height": 8.208606675589806,
			"seed": 976055313,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.7137948445087545
				],
				[
					0,
					-0.3569042295065117
				],
				[
					0,
					0
				],
				[
					0,
					0.7137812300044573
				],
				[
					0,
					1.070685459510969
				],
				[
					0,
					1.4275760745131834
				],
				[
					0,
					2.141370919021938
				],
				[
					0,
					2.4982615340241523
				],
				[
					0,
					3.212056378532907
				],
				[
					0,
					3.5689606080394185
				],
				[
					0,
					3.925851223041633
				],
				[
					0,
					4.639646067550387
				],
				[
					0,
					4.996536682552602
				],
				[
					0,
					5.710331527061356
				],
				[
					0,
					6.067222142063571
				],
				[
					0,
					6.781016986572325
				],
				[
					0,
					7.137921216078837
				],
				[
					0,
					7.494811831081051
				],
				[
					0,
					7.494811831081051
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 200,
			"versionNonce": 630366973,
			"isDeleted": false,
			"id": "JQ9WqPJWAp_8Hqf_pOdtr",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2193.998212876104,
			"y": -62.27061656784639,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 10.349991209115615,
			"height": 4.639646067550387,
			"seed": 715734897,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3568906150021576,
					0
				],
				[
					0.7137812300043151,
					0
				],
				[
					0.7137812300043151,
					0.7137948445087545
				],
				[
					1.427589689017168,
					0.7137948445087545
				],
				[
					1.427589689017168,
					1.070685459510969
				],
				[
					1.7844803040193256,
					1.7844803040197235
				],
				[
					1.7844803040193256,
					2.141384533526235
				],
				[
					2.4982615340240955,
					2.141384533526235
				],
				[
					2.4982615340240955,
					2.4982751485284496
				],
				[
					2.4982615340240955,
					3.212069993037204
				],
				[
					2.855152149026253,
					3.212069993037204
				],
				[
					2.855152149026253,
					3.5689606080394185
				],
				[
					3.568960608039106,
					4.282755452548173
				],
				[
					3.9258512230412634,
					4.639646067550387
				],
				[
					4.282741838043876,
					4.639646067550387
				],
				[
					4.996550297056729,
					4.639646067550387
				],
				[
					5.353440912058886,
					4.639646067550387
				],
				[
					6.067222142063201,
					3.92586483754593
				],
				[
					6.424112757065814,
					3.92586483754593
				],
				[
					6.424112757065814,
					3.5689606080394185
				],
				[
					7.1379212160786665,
					3.5689606080394185
				],
				[
					7.1379212160786665,
					2.8551657635306924
				],
				[
					7.494811831080824,
					2.8551657635306924
				],
				[
					7.851702446082982,
					2.4982751485284496
				],
				[
					8.56551090509629,
					2.4982751485284496
				],
				[
					8.56551090509629,
					2.141384533526235
				],
				[
					8.922401520098447,
					2.141384533526235
				],
				[
					9.636182750102762,
					1.4275896890174806
				],
				[
					9.99307336510492,
					1.4275896890174806
				],
				[
					9.99307336510492,
					1.070685459510969
				],
				[
					10.349991209115615,
					1.070685459510969
				],
				[
					10.349991209115615,
					1.070685459510969
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 153,
			"versionNonce": 748345171,
			"isDeleted": false,
			"id": "CO9wOhnd9ADz5LHqGWC1U",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2200.779216248172,
			"y": -131.86534842461506,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 14.275842432157788,
			"height": 12.491362128137965,
			"seed": 1843524703,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.0706718450069275,
					0
				],
				[
					-1.7844803040197803,
					0.35689061500222863
				],
				[
					-2.141370919021938,
					0.7137948445087403
				],
				[
					-3.212069993037403,
					1.4275760745131976
				],
				[
					-4.282741838043876,
					2.855165763530678
				],
				[
					-5.7103315270614985,
					3.925851223041647
				],
				[
					-6.781030601076964,
					4.639646067550387
				],
				[
					-8.208593061085594,
					6.424126371570097
				],
				[
					-9.279292135101059,
					7.494811831081066
				],
				[
					-10.34999120911607,
					8.208606675589806
				],
				[
					-11.420663054122997,
					9.279292135100775
				],
				[
					-12.491362128138007,
					10.349977594611744
				],
				[
					-13.205143358142777,
					11.420676668626996
				],
				[
					-13.91895181715563,
					11.777567283629224
				],
				[
					-14.275842432157788,
					11.777567283629224
				],
				[
					-14.275842432157788,
					12.491362128137965
				],
				[
					-14.275842432157788,
					12.491362128137965
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 159,
			"versionNonce": 547306333,
			"isDeleted": false,
			"id": "MDVyGXXb1qTxM0IXTOp0l",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2218.2671286733666,
			"y": -129.36707327608661,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.0706990740150104,
			"height": 14.632733047159903,
			"seed": 470888625,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3568906150021576,
					0
				],
				[
					0.3568906150021576,
					0.35689061500222863
				],
				[
					0.3568906150021576,
					1.070685459510969
				],
				[
					0.3568906150021576,
					1.4275760745131976
				],
				[
					0.3568906150021576,
					2.4982615340241665
				],
				[
					0.3568906150021576,
					3.212056378532907
				],
				[
					0.3568906150021576,
					4.639646067550387
				],
				[
					0.3568906150021576,
					5.710331527061356
				],
				[
					0.3568906150021576,
					6.424126371570097
				],
				[
					0.3568906150021576,
					7.137921216078837
				],
				[
					1.0706990740150104,
					8.208606675589806
				],
				[
					1.0706990740150104,
					8.565497290592035
				],
				[
					1.0706990740150104,
					9.636182750103004
				],
				[
					1.0706990740150104,
					9.993086979609515
				],
				[
					1.0706990740150104,
					10.706881824118256
				],
				[
					1.0706990740150104,
					11.063772439120484
				],
				[
					1.0706990740150104,
					12.134457898631453
				],
				[
					0.7137812300043151,
					12.848252743140193
				],
				[
					0.7137812300043151,
					13.205143358142422
				],
				[
					0.7137812300043151,
					13.562047587648934
				],
				[
					0.7137812300043151,
					14.275842432157674
				],
				[
					0.7137812300043151,
					14.632733047159903
				],
				[
					0.7137812300043151,
					14.632733047159903
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 168,
			"versionNonce": 680162547,
			"isDeleted": false,
			"id": "ewYlpA5DFPmRJ06P5YrI5",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2211.8429886872923,
			"y": -118.30330083696613,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 13.562061202153018,
			"height": 5.710331527061356,
			"seed": 2016661393,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.35691784401069526,
					0
				],
				[
					0.7138084590128528,
					0
				],
				[
					1.4275896890176227,
					0
				],
				[
					1.7844803040197803,
					0
				],
				[
					2.1413981480304756,
					0.7137948445087403
				],
				[
					2.1413981480304756,
					1.070685459510969
				],
				[
					2.8551793780347907,
					1.7844803040197093
				],
				[
					3.2120699930369483,
					2.4982751485284496
				],
				[
					3.925878452050256,
					3.21206999303719
				],
				[
					4.2827690670524134,
					3.5689606080394185
				],
				[
					4.2827690670524134,
					4.282755452548159
				],
				[
					4.639659682054571,
					4.282755452548159
				],
				[
					4.639659682054571,
					4.639646067550387
				],
				[
					5.353440912058886,
					4.639646067550387
				],
				[
					5.710358756069581,
					4.639646067550387
				],
				[
					6.424139986074351,
					4.639646067550387
				],
				[
					6.781030601076509,
					4.639646067550387
				],
				[
					7.494839060089362,
					4.639646067550387
				],
				[
					7.851729675091519,
					3.925851223041647
				],
				[
					8.922401520098447,
					2.855165763530678
				],
				[
					9.279319364109142,
					2.4982751485284496
				],
				[
					9.993100594113457,
					2.141370919021938
				],
				[
					10.34999120911607,
					1.070685459510969
				],
				[
					11.063799668128922,
					0.35689061500222863
				],
				[
					11.42069028313108,
					0.35689061500222863
				],
				[
					11.777580898133237,
					0
				],
				[
					11.777580898133237,
					-0.7137948445087403
				],
				[
					12.491362128138007,
					-0.7137948445087403
				],
				[
					12.848279972148703,
					-0.7137948445087403
				],
				[
					12.848279972148703,
					-1.070685459510969
				],
				[
					13.562061202153018,
					-1.070685459510969
				],
				[
					13.562061202153018,
					-1.070685459510969
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 156,
			"versionNonce": 1396295613,
			"isDeleted": false,
			"id": "7_KtACCNIE45GiutgejXM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2228.6171198824827,
			"y": -129.0101826610844,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 17.487912425194736,
			"height": 10.706881824118256,
			"seed": 657555007,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.4275896890176227,
					0
				],
				[
					-1.7844803040197803,
					0.35689061500222863
				],
				[
					-2.498288763033088,
					0.35689061500222863
				],
				[
					-3.5689606080395606,
					1.070685459510969
				],
				[
					-4.2827690670524134,
					1.7844803040197093
				],
				[
					-6.067249371072194,
					2.855165763530678
				],
				[
					-7.494811831081279,
					4.282755452548159
				],
				[
					-8.922401520098902,
					5.353440912059128
				],
				[
					-10.706881824118227,
					6.424126371570097
				],
				[
					-11.06377243912084,
					6.781030601076608
				],
				[
					-12.491362128138007,
					7.851716060587577
				],
				[
					-13.562061202153473,
					8.208606675589806
				],
				[
					-14.98965089117064,
					9.279292135100775
				],
				[
					-16.060322736177568,
					9.993086979609515
				],
				[
					-16.060322736177568,
					10.349991209116027
				],
				[
					-16.77413119519042,
					10.349991209116027
				],
				[
					-17.13102181019258,
					10.349991209116027
				],
				[
					-17.13102181019258,
					10.706881824118256
				],
				[
					-17.487912425194736,
					10.706881824118256
				],
				[
					-17.487912425194736,
					10.706881824118256
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 161,
			"versionNonce": 1811242643,
			"isDeleted": false,
			"id": "D136NYCqTaDFVhc5ibmbs",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2245.034333233662,
			"y": -132.5791432691238,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.0706990740154652,
			"height": 12.848252743140193,
			"seed": 714930257,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3568906150026123,
					0
				],
				[
					0.3568906150026123,
					0.7137948445087403
				],
				[
					0.3568906150026123,
					1.070685459510969
				],
				[
					0.3568906150026123,
					1.7844803040197093
				],
				[
					0.3568906150026123,
					2.141370919021938
				],
				[
					0.3568906150026123,
					3.21206999303719
				],
				[
					0.3568906150026123,
					3.5689606080394185
				],
				[
					1.0706990740154652,
					4.639646067550387
				],
				[
					1.0706990740154652,
					5.353440912059128
				],
				[
					1.0706990740154652,
					5.710331527061356
				],
				[
					1.0706990740154652,
					6.067235756567868
				],
				[
					1.0706990740154652,
					6.781030601076608
				],
				[
					1.0706990740154652,
					7.137921216078837
				],
				[
					1.0706990740154652,
					7.851716060587577
				],
				[
					1.0706990740154652,
					8.208606675589806
				],
				[
					1.0706990740154652,
					8.922401520098546
				],
				[
					1.0706990740154652,
					9.279292135100775
				],
				[
					1.0706990740154652,
					9.636196364607287
				],
				[
					0.7137812300047699,
					10.349991209116027
				],
				[
					0.7137812300047699,
					10.706881824118256
				],
				[
					0.7137812300047699,
					11.420676668626996
				],
				[
					0.7137812300047699,
					11.777567283629224
				],
				[
					0.7137812300047699,
					12.134471513135736
				],
				[
					0.7137812300047699,
					12.848252743140193
				],
				[
					0.7137812300047699,
					12.848252743140193
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 163,
			"versionNonce": 2139342877,
			"isDeleted": false,
			"id": "48V5eRU961wQGJJlcDNht",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2240.751591395618,
			"y": -122.94294690451652,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 9.636182750103217,
			"height": 4.639646067550387,
			"seed": 1120955121,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7137812300047699,
					0
				],
				[
					0.7137812300047699,
					0.7137948445087403
				],
				[
					0.7137812300047699,
					1.070685459510969
				],
				[
					1.0706718450069275,
					1.7844803040197093
				],
				[
					1.0706718450069275,
					2.141370919021938
				],
				[
					1.7844803040197803,
					2.4982751485284496
				],
				[
					1.7844803040197803,
					3.212056378532907
				],
				[
					2.141370919021938,
					3.5689606080394185
				],
				[
					2.8551521490267078,
					4.282755452548159
				],
				[
					3.2120427640288653,
					4.282755452548159
				],
				[
					3.2120427640288653,
					4.639646067550387
				],
				[
					3.5689606080395606,
					4.639646067550387
				],
				[
					4.282741838043876,
					4.639646067550387
				],
				[
					4.639632453046488,
					4.639646067550387
				],
				[
					5.353440912059341,
					4.639646067550387
				],
				[
					5.7103315270614985,
					4.639646067550387
				],
				[
					6.424112757065814,
					3.925851223041647
				],
				[
					6.781003372068426,
					3.925851223041647
				],
				[
					6.781003372068426,
					3.5689606080394185
				],
				[
					7.137921216079121,
					3.5689606080394185
				],
				[
					7.851702446083436,
					2.855165763530678
				],
				[
					8.208593061085594,
					2.4982751485284496
				],
				[
					8.922401520098902,
					2.141370919021938
				],
				[
					9.279292135101059,
					2.141370919021938
				],
				[
					9.279292135101059,
					1.4275760745131976
				],
				[
					9.636182750103217,
					1.4275760745131976
				],
				[
					9.636182750103217,
					1.4275760745131976
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 169,
			"versionNonce": 26350643,
			"isDeleted": false,
			"id": "4F9S6i1AoRzS94cNNnyds",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2193.641295032093,
			"y": -139.71706448520263,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 17.13102181019258,
			"height": 5.353440912059128,
			"seed": 1784731025,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.7137948445087403
				],
				[
					0.3568906150021576,
					-0.7137948445087403
				],
				[
					0.3568906150021576,
					-1.070685459510969
				],
				[
					0.7137812300043151,
					-1.070685459510969
				],
				[
					0.7137812300043151,
					-1.7844803040197093
				],
				[
					1.4275896890176227,
					-1.7844803040197093
				],
				[
					1.7844803040197803,
					-2.141370919021952
				],
				[
					2.4982615340240955,
					-2.141370919021952
				],
				[
					2.4982615340240955,
					-2.4982751485284496
				],
				[
					2.8551793780347907,
					-2.4982751485284496
				],
				[
					3.212069993037403,
					-2.4982751485284496
				],
				[
					3.212069993037403,
					-3.21206999303719
				],
				[
					3.925851223041718,
					-3.21206999303719
				],
				[
					4.282741838043876,
					-3.21206999303719
				],
				[
					4.282741838043876,
					-3.5689606080394185
				],
				[
					4.996550297056729,
					-3.5689606080394185
				],
				[
					5.353440912059341,
					-4.282755452548159
				],
				[
					6.067222142063656,
					-4.282755452548159
				],
				[
					6.067222142063656,
					-4.639646067550387
				],
				[
					6.424139986074351,
					-4.639646067550387
				],
				[
					6.781030601076509,
					-4.639646067550387
				],
				[
					7.494811831081279,
					-4.639646067550387
				],
				[
					7.851702446083436,
					-4.639646067550387
				],
				[
					8.56551090509629,
					-4.639646067550387
				],
				[
					8.922401520098447,
					-4.639646067550387
				],
				[
					9.279292135100604,
					-4.639646067550387
				],
				[
					9.993100594113912,
					-3.9258512230416613
				],
				[
					11.063772439120385,
					-3.5689606080394185
				],
				[
					11.420663054122542,
					-2.855165763530678
				],
				[
					12.13447151313585,
					-2.855165763530678
				],
				[
					13.205143358142323,
					-2.4982751485284496
				],
				[
					13.562061202153018,
					-1.7844803040197093
				],
				[
					14.275842432157788,
					-1.7844803040197093
				],
				[
					14.632733047159945,
					-1.4275896890174806
				],
				[
					14.989623662162103,
					-1.4275896890174806
				],
				[
					14.989623662162103,
					-1.070685459510969
				],
				[
					15.703432121174956,
					-1.070685459510969
				],
				[
					15.703432121174956,
					-0.35689061500224284
				],
				[
					16.060322736177568,
					-0.35689061500224284
				],
				[
					16.060322736177568,
					0
				],
				[
					16.774103966181883,
					0
				],
				[
					16.774103966181883,
					0.7137948445087403
				],
				[
					17.13102181019258,
					0.7137948445087403
				],
				[
					17.13102181019258,
					0.7137948445087403
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 153,
			"versionNonce": 661568637,
			"isDeleted": false,
			"id": "kSdA_9Uid3bHzBEsMPAUE",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2206.489547775233,
			"y": -138.64637902569166,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 6.781030601076509,
			"height": 8.208620290094075,
			"seed": 1366462417,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3568906150021576,
					0
				],
				[
					0.7138084590128528,
					0
				],
				[
					1.7844803040197803,
					0.7137948445087403
				],
				[
					2.141370919021938,
					1.070685459510969
				],
				[
					2.8551793780347907,
					1.070685459510969
				],
				[
					3.925851223041718,
					1.4275896890174806
				],
				[
					4.2827690670524134,
					2.1413845335262067
				],
				[
					4.996550297057183,
					2.1413845335262067
				],
				[
					5.353440912059341,
					2.1413845335262067
				],
				[
					5.7103315270614985,
					2.1413845335262067
				],
				[
					6.424139986074351,
					2.1413845335262067
				],
				[
					6.424139986074351,
					1.7844803040197093
				],
				[
					6.781030601076509,
					1.7844803040197093
				],
				[
					6.781030601076509,
					1.4275896890174806
				],
				[
					6.781030601076509,
					1.070685459510969
				],
				[
					6.781030601076509,
					0.3569042295064975
				],
				[
					6.781030601076509,
					0
				],
				[
					6.781030601076509,
					-0.7137948445087403
				],
				[
					6.781030601076509,
					-1.070685459510969
				],
				[
					6.781030601076509,
					-1.7844803040197093
				],
				[
					6.781030601076509,
					-2.4982751485284496
				],
				[
					6.781030601076509,
					-3.5689606080394185
				],
				[
					6.781030601076509,
					-4.282755452548159
				],
				[
					6.781030601076509,
					-4.639646067550387
				],
				[
					6.781030601076509,
					-5.353440912059128
				],
				[
					6.781030601076509,
					-5.710331527061356
				],
				[
					6.781030601076509,
					-6.067235756567868
				],
				[
					6.781030601076509,
					-6.067235756567868
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 172,
			"versionNonce": 1497830867,
			"isDeleted": false,
			"id": "o9Q8U7ZyqsatkBnrwjZ2D",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2219.337800518373,
			"y": -137.2187893366742,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 23.55516179626693,
			"height": 8.20860667558982,
			"seed": 737090577,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.3569042295065117
				],
				[
					0,
					-1.0706854595109832
				],
				[
					0,
					-1.4275896890174806
				],
				[
					0.7138084590128528,
					-2.141384533526221
				],
				[
					1.0706990740154652,
					-2.141384533526221
				],
				[
					1.7844803040197803,
					-2.4982751485284496
				],
				[
					2.1413981480304756,
					-3.21206999303719
				],
				[
					2.498288763032633,
					-3.5689606080394185
				],
				[
					3.5689606080395606,
					-3.92586483754593
				],
				[
					4.2827690670524134,
					-3.92586483754593
				],
				[
					4.639659682054571,
					-4.639646067550402
				],
				[
					5.710358756070036,
					-4.996550297056899
				],
				[
					6.067249371072194,
					-5.710345141565639
				],
				[
					7.1379212160786665,
					-6.067235756567868
				],
				[
					8.208620290094132,
					-6.781030601076608
				],
				[
					9.279319364109597,
					-6.781030601076608
				],
				[
					10.34999120911607,
					-7.137921216078837
				],
				[
					10.706881824118227,
					-7.494825445585349
				],
				[
					11.420690283131535,
					-7.494825445585349
				],
				[
					11.777580898133692,
					-7.494825445585349
				],
				[
					12.13447151313585,
					-7.494825445585349
				],
				[
					13.20517058715086,
					-7.494825445585349
				],
				[
					13.91895181715563,
					-7.494825445585349
				],
				[
					14.98965089117064,
					-8.20860667558982
				],
				[
					15.346541506173253,
					-8.20860667558982
				],
				[
					15.70343212117541,
					-8.20860667558982
				],
				[
					16.417240580188263,
					-7.851716060587577
				],
				[
					16.77413119519042,
					-7.851716060587577
				],
				[
					17.48791242519519,
					-7.494825445585349
				],
				[
					17.84480304019735,
					-7.494825445585349
				],
				[
					18.201720884208044,
					-7.494825445585349
				],
				[
					18.91550211421236,
					-7.137921216078837
				],
				[
					19.272392729214516,
					-6.424126371570111
				],
				[
					19.986201188227824,
					-6.424126371570111
				],
				[
					20.34309180322998,
					-6.067235756567868
				],
				[
					21.056873033234297,
					-6.067235756567868
				],
				[
					21.056873033234297,
					-5.353440912059128
				],
				[
					21.413763648236454,
					-5.353440912059128
				],
				[
					21.413763648236454,
					-4.996550297056899
				],
				[
					21.77068149224715,
					-4.282755452548159
				],
				[
					22.48446272225192,
					-3.92586483754593
				],
				[
					22.48446272225192,
					-3.5689606080394185
				],
				[
					22.841353337254077,
					-2.8551657635306924
				],
				[
					23.55516179626693,
					-2.4982751485284496
				],
				[
					23.55516179626693,
					-1.7844803040197093
				],
				[
					23.55516179626693,
					-1.4275896890174806
				],
				[
					23.55516179626693,
					-1.4275896890174806
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 152,
			"versionNonce": 314320093,
			"isDeleted": false,
			"id": "ey60JmURMgSq-jd-1KwaB",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2237.8964120175833,
			"y": -137.5756935661807,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 6.781030601076509,
			"height": 6.781030601076608,
			"seed": 1588587505,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3568906150021576,
					0
				],
				[
					0.7137812300043151,
					0
				],
				[
					1.4275896890176227,
					0
				],
				[
					1.7844803040197803,
					0
				],
				[
					2.4982615340240955,
					0
				],
				[
					2.4982615340240955,
					0.3569042295065117
				],
				[
					2.855152149026253,
					0.3569042295065117
				],
				[
					3.2120699930369483,
					1.0706990740152378
				],
				[
					3.925851223041718,
					1.0706990740152378
				],
				[
					4.282741838043876,
					1.0706990740152378
				],
				[
					4.282741838043876,
					1.4275896890174806
				],
				[
					4.996550297056729,
					1.4275896890174806
				],
				[
					4.996550297056729,
					0.7137948445087403
				],
				[
					5.353440912058886,
					0.7137948445087403
				],
				[
					5.353440912058886,
					0
				],
				[
					6.067222142063656,
					-0.7137812300044715
				],
				[
					6.067222142063656,
					-1.070685459510969
				],
				[
					6.067222142063656,
					-1.7844803040197093
				],
				[
					6.067222142063656,
					-2.141370919021938
				],
				[
					6.067222142063656,
					-2.855165763530678
				],
				[
					6.067222142063656,
					-3.212056378532907
				],
				[
					6.424112757065814,
					-3.5689606080394185
				],
				[
					6.424112757065814,
					-4.28274183804389
				],
				[
					6.781030601076509,
					-4.28274183804389
				],
				[
					6.781030601076509,
					-4.639646067550387
				],
				[
					6.781030601076509,
					-5.353440912059128
				],
				[
					6.781030601076509,
					-5.353440912059128
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 144,
			"versionNonce": 573236083,
			"isDeleted": false,
			"id": "QYNRuTuJWGFLLyRGRi8Nh",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2205.7757665452286,
			"y": -68.33785232441426,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 11.777580898133692,
			"height": 4.996550297056899,
			"seed": 1644484415,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.7138084590133076,
					0
				],
				[
					-1.0706990740154652,
					0
				],
				[
					-1.7844803040197803,
					0.3568906150022144
				],
				[
					-2.141370919021938,
					1.070685459510969
				],
				[
					-2.498288763032633,
					1.070685459510969
				],
				[
					-2.498288763032633,
					1.4275896890174806
				],
				[
					-3.212069993037403,
					1.4275896890174806
				],
				[
					-4.639659682054571,
					2.141370919021938
				],
				[
					-4.639659682054571,
					2.4982751485284496
				],
				[
					-5.353440912059341,
					2.4982751485284496
				],
				[
					-5.7103315270614985,
					3.2120699930371757
				],
				[
					-6.067249371072194,
					3.2120699930371757
				],
				[
					-7.137921216079121,
					3.5689606080394185
				],
				[
					-8.208620290094132,
					3.925851223041633
				],
				[
					-9.279292135101059,
					3.925851223041633
				],
				[
					-9.636209979111754,
					4.639646067550387
				],
				[
					-10.706881824118227,
					4.639646067550387
				],
				[
					-11.777580898133692,
					4.996550297056899
				],
				[
					-11.777580898133692,
					4.996550297056899
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 148,
			"versionNonce": 352158013,
			"isDeleted": false,
			"id": "o3h8OlNrI9PUBRmORUGDy",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2226.475721734452,
			"y": -70.8361274729427,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.0706990740154652,
			"height": 13.56204758764892,
			"seed": 1532854161,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					1.4275896890174806
				],
				[
					0,
					1.784480304019695
				],
				[
					0,
					2.4982751485284496
				],
				[
					0,
					2.855165763530664
				],
				[
					0,
					3.92586483754593
				],
				[
					0,
					4.282755452548145
				],
				[
					0.7138084590133076,
					4.996550297056899
				],
				[
					0.7138084590133076,
					5.3534409120591135
				],
				[
					0.7138084590133076,
					6.067235756567868
				],
				[
					1.0706990740154652,
					6.4241263715700825
				],
				[
					1.0706990740154652,
					6.781030601076594
				],
				[
					1.0706990740154652,
					7.851716060587563
				],
				[
					1.0706990740154652,
					8.565510905096318
				],
				[
					1.0706990740154652,
					9.636196364607287
				],
				[
					1.0706990740154652,
					9.993086979609501
				],
				[
					1.0706990740154652,
					10.349991209116013
				],
				[
					1.0706990740154652,
					11.063786053624767
				],
				[
					1.0706990740154652,
					11.420676668626982
				],
				[
					1.0706990740154652,
					12.134471513135736
				],
				[
					1.0706990740154652,
					12.49136212813795
				],
				[
					1.0706990740154652,
					13.205156972646705
				],
				[
					1.0706990740154652,
					13.56204758764892
				],
				[
					1.0706990740154652,
					13.56204758764892
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 160,
			"versionNonce": 1686371603,
			"isDeleted": false,
			"id": "WzzMqd6D_fioOBl8UQSCx",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2221.4791986664036,
			"y": -60.843040493333206,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 13.918924588147092,
			"height": 5.710345141565625,
			"seed": 387490417,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7137812300043151,
					0
				],
				[
					1.0706718450069275,
					0
				],
				[
					1.0706718450069275,
					0.3569042295065117
				],
				[
					1.0706718450069275,
					1.0706990740152662
				],
				[
					1.7844803040197803,
					1.0706990740152662
				],
				[
					1.7844803040197803,
					1.4275896890174806
				],
				[
					2.141370919021938,
					1.4275896890174806
				],
				[
					2.141370919021938,
					2.141384533526235
				],
				[
					2.4982615340240955,
					2.4982751485284496
				],
				[
					3.2120427640288653,
					2.4982751485284496
				],
				[
					3.2120427640288653,
					3.212069993037204
				],
				[
					3.5689606080395606,
					3.212069993037204
				],
				[
					3.5689606080395606,
					3.5689606080394185
				],
				[
					4.282741838043876,
					3.5689606080394185
				],
				[
					4.639632453046033,
					3.5689606080394185
				],
				[
					4.639632453046033,
					3.92586483754593
				],
				[
					4.996523068048191,
					3.92586483754593
				],
				[
					5.7103315270614985,
					3.92586483754593
				],
				[
					6.067222142063656,
					3.92586483754593
				],
				[
					6.781003372067971,
					3.92586483754593
				],
				[
					7.137921216079121,
					3.92586483754593
				],
				[
					7.851702446083436,
					3.5689606080394185
				],
				[
					8.922401520098447,
					2.8551793780349612
				],
				[
					9.993073365105374,
					1.7844803040197235
				],
				[
					10.706881824118227,
					1.4275896890174806
				],
				[
					10.706881824118227,
					0.3569042295065117
				],
				[
					11.420663054122997,
					-0.3568906150022144
				],
				[
					11.777553669125155,
					-0.3568906150022144
				],
				[
					12.491362128138007,
					-0.7137812300044573
				],
				[
					12.491362128138007,
					-1.070685459510969
				],
				[
					12.848252743140165,
					-1.070685459510969
				],
				[
					13.562033973144935,
					-1.070685459510969
				],
				[
					13.562033973144935,
					-1.784480304019695
				],
				[
					13.918924588147092,
					-1.784480304019695
				],
				[
					13.918924588147092,
					-1.784480304019695
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 147,
			"versionNonce": 328487325,
			"isDeleted": false,
			"id": "c5vnYvmCMK7zX_cCYvogS",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2253.2429262947476,
			"y": -131.86534842461506,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 21.05684580422576,
			"height": 11.063772439120484,
			"seed": 1238460863,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.0706718450064727,
					0
				],
				[
					-1.4275624600086303,
					0.35689061500222863
				],
				[
					-2.141370919021938,
					0.35689061500222863
				],
				[
					-3.2120427640284106,
					0.7137948445087403
				],
				[
					-4.639632453046033,
					1.7844803040197093
				],
				[
					-6.067222142063656,
					2.855165763530678
				],
				[
					-8.565483676087752,
					3.925851223041647
				],
				[
					-9.279292135100604,
					4.282755452548159
				],
				[
					-10.706881824118227,
					5.353440912059128
				],
				[
					-12.848252743140165,
					6.067235756567868
				],
				[
					-14.989623662162103,
					7.494811831081066
				],
				[
					-16.060322736177113,
					7.851716060587577
				],
				[
					-17.4878851961862,
					8.565497290592035
				],
				[
					-18.55858427020121,
					8.922401520098546
				],
				[
					-18.91547488520382,
					9.636196364607287
				],
				[
					-19.629283344216674,
					9.993086979609515
				],
				[
					-19.98617395921883,
					9.993086979609515
				],
				[
					-19.98617395921883,
					10.349977594611744
				],
				[
					-20.34306457422099,
					10.349977594611744
				],
				[
					-20.34306457422099,
					11.063772439120484
				],
				[
					-21.05684580422576,
					11.063772439120484
				],
				[
					-21.05684580422576,
					11.063772439120484
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 150,
			"versionNonce": 1539891891,
			"isDeleted": false,
			"id": "BjEGzCVxmZItTU2tOmcMw",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2280.723939314056,
			"y": -132.22225265412158,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.7844803040197803,
			"height": 14.632746661664186,
			"seed": 1770312369,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.3569042295065117
				],
				[
					-0.7138084590128528,
					1.070699074015252
				],
				[
					-0.7138084590128528,
					1.4275896890174806
				],
				[
					-0.7138084590128528,
					2.4982751485284496
				],
				[
					-1.0706990740150104,
					3.21206999303719
				],
				[
					-1.0706990740150104,
					3.5689606080394185
				],
				[
					-1.0706990740150104,
					3.92586483754593
				],
				[
					-1.0706990740150104,
					4.6396596820546705
				],
				[
					-1.0706990740150104,
					5.710345141565639
				],
				[
					-1.0706990740150104,
					6.781030601076608
				],
				[
					-1.0706990740150104,
					7.137921216078837
				],
				[
					-1.0706990740150104,
					7.494825445585349
				],
				[
					-1.0706990740150104,
					8.208620290094089
				],
				[
					-1.0706990740150104,
					8.565510905096318
				],
				[
					-1.7844803040197803,
					9.279305749605058
				],
				[
					-1.7844803040197803,
					9.993100594113798
				],
				[
					-1.7844803040197803,
					10.706881824118256
				],
				[
					-1.7844803040197803,
					11.777580898133508
				],
				[
					-1.7844803040197803,
					12.134471513135736
				],
				[
					-1.7844803040197803,
					12.848266357644476
				],
				[
					-1.7844803040197803,
					13.205156972646705
				],
				[
					-1.7844803040197803,
					13.562061202153217
				],
				[
					-1.7844803040197803,
					14.275842432157674
				],
				[
					-1.7844803040197803,
					14.632746661664186
				],
				[
					-1.7844803040197803,
					14.632746661664186
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 154,
			"versionNonce": 1269962237,
			"isDeleted": false,
			"id": "MACRbCd-uzxI6vHnyUtkE",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2273.5860180979776,
			"y": -118.66019145196836,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 8.56551090509629,
			"height": 6.067235756567868,
			"seed": 985186641,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.3569042295065117
				],
				[
					0,
					0
				],
				[
					0.7137812300043151,
					0.7137812300044573
				],
				[
					1.0706718450064727,
					1.070685459510969
				],
				[
					1.0706718450064727,
					1.7844803040197093
				],
				[
					1.4275896890176227,
					2.141370919021938
				],
				[
					2.141370919021938,
					2.855165763530678
				],
				[
					2.141370919021938,
					3.212056378532907
				],
				[
					2.141370919021938,
					3.5689606080394185
				],
				[
					2.4982615340240955,
					3.5689606080394185
				],
				[
					3.2120699930369483,
					4.639646067550387
				],
				[
					3.5689606080395606,
					4.639646067550387
				],
				[
					3.5689606080395606,
					5.353440912059128
				],
				[
					4.282741838043876,
					5.353440912059128
				],
				[
					4.282741838043876,
					5.710331527061356
				],
				[
					4.639632453046033,
					5.710331527061356
				],
				[
					4.996550297056729,
					5.710331527061356
				],
				[
					5.7103315270614985,
					5.710331527061356
				],
				[
					5.7103315270614985,
					4.996536682552616
				],
				[
					5.7103315270614985,
					4.639646067550387
				],
				[
					6.781030601076509,
					3.925851223041647
				],
				[
					7.1379212160786665,
					3.5689606080394185
				],
				[
					7.1379212160786665,
					3.212056378532907
				],
				[
					7.851702446083436,
					2.4982615340241665
				],
				[
					7.851702446083436,
					2.141370919021938
				],
				[
					8.208593061085594,
					2.141370919021938
				],
				[
					8.208593061085594,
					1.4275760745131976
				],
				[
					8.56551090509629,
					1.070685459510969
				],
				[
					8.56551090509629,
					1.070685459510969
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 179,
			"versionNonce": 278926419,
			"isDeleted": false,
			"id": "aBzRYVjkheMyoDmh4FKCB",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2253.5998441387583,
			"y": -143.6429157082443,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 19.27236550020598,
			"height": 11.063786053624767,
			"seed": 47332689,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.3569042295064975
				],
				[
					0.7137812300047699,
					-1.0706990740152378
				],
				[
					1.427562460009085,
					-1.4275896890174664
				],
				[
					2.141370919021938,
					-1.4275896890174664
				],
				[
					2.49826153402455,
					-2.1413845335262067
				],
				[
					3.2120427640288653,
					-2.1413845335262067
				],
				[
					3.5689606080395606,
					-2.4982751485284496
				],
				[
					4.282741838043876,
					-2.4982751485284496
				],
				[
					4.639632453046488,
					-3.2120699930371757
				],
				[
					5.7103315270614985,
					-3.2120699930371757
				],
				[
					6.067222142063656,
					-3.5689606080394185
				],
				[
					6.781003372068426,
					-3.925864837545916
				],
				[
					7.494811831081279,
					-3.925864837545916
				],
				[
					8.208593061085594,
					-4.639659682054656
				],
				[
					8.565483676088206,
					-4.639659682054656
				],
				[
					9.279292135101059,
					-4.639659682054656
				],
				[
					10.349963980107532,
					-4.996550297056885
				],
				[
					10.706881824118227,
					-4.996550297056885
				],
				[
					11.06377243912084,
					-5.710345141565625
				],
				[
					12.134444284127312,
					-6.067235756567868
				],
				[
					13.205143358142777,
					-6.067235756567868
				],
				[
					13.918924588147092,
					-6.067235756567868
				],
				[
					13.918924588147092,
					-6.4241399860743655
				],
				[
					14.275842432157788,
					-6.4241399860743655
				],
				[
					14.632733047159945,
					-6.4241399860743655
				],
				[
					15.346514277164715,
					-6.4241399860743655
				],
				[
					15.703404892166873,
					-6.4241399860743655
				],
				[
					16.417213351179726,
					-6.4241399860743655
				],
				[
					16.774103966181883,
					-6.4241399860743655
				],
				[
					16.774103966181883,
					-6.067235756567868
				],
				[
					16.774103966181883,
					-5.353440912059128
				],
				[
					17.13099458118404,
					-4.996550297056885
				],
				[
					17.13099458118404,
					-4.282755452548159
				],
				[
					17.84480304019735,
					-3.925864837545916
				],
				[
					17.84480304019735,
					-3.5689606080394185
				],
				[
					17.84480304019735,
					-2.855179378034947
				],
				[
					17.84480304019735,
					-2.4982751485284496
				],
				[
					17.84480304019735,
					-1.7844803040197093
				],
				[
					18.201693655199506,
					-1.7844803040197093
				],
				[
					18.201693655199506,
					-1.4275896890174664
				],
				[
					18.201693655199506,
					-0.7137948445087261
				],
				[
					18.201693655199506,
					-0.3569042295064975
				],
				[
					18.201693655199506,
					0
				],
				[
					18.201693655199506,
					0.7137812300044715
				],
				[
					18.201693655199506,
					1.0706854595109832
				],
				[
					18.201693655199506,
					1.7844803040197093
				],
				[
					18.91547488520382,
					2.141370919021952
				],
				[
					18.91547488520382,
					2.8551657635306924
				],
				[
					18.91547488520382,
					3.212056378532921
				],
				[
					18.91547488520382,
					3.5689606080394185
				],
				[
					18.91547488520382,
					4.28274183804389
				],
				[
					18.91547488520382,
					4.639646067550402
				],
				[
					19.27236550020598,
					4.639646067550402
				],
				[
					19.27236550020598,
					4.639646067550402
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 153,
			"versionNonce": 1482182237,
			"isDeleted": false,
			"id": "SEa10gL5B2FYT6yjwUBVD",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2267.875686570916,
			"y": -141.14465417422014,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 9.279292135101059,
			"height": 3.92586483754593,
			"seed": 935155281,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3568906150021576,
					0.3569042295065117
				],
				[
					1.0706718450069275,
					0.7137948445087403
				],
				[
					1.427562460009085,
					1.0706990740152378
				],
				[
					2.141370919021938,
					1.0706990740152378
				],
				[
					2.141370919021938,
					1.7844803040197093
				],
				[
					2.4982615340240955,
					1.7844803040197093
				],
				[
					2.4982615340240955,
					2.141384533526221
				],
				[
					2.855152149026253,
					2.141384533526221
				],
				[
					2.855152149026253,
					2.855179378034947
				],
				[
					3.5689606080395606,
					2.855179378034947
				],
				[
					3.5689606080395606,
					3.21206999303719
				],
				[
					3.925851223041718,
					3.21206999303719
				],
				[
					3.925851223041718,
					3.92586483754593
				],
				[
					4.639632453046033,
					3.92586483754593
				],
				[
					4.996523068048191,
					3.92586483754593
				],
				[
					5.7103315270614985,
					3.92586483754593
				],
				[
					6.067222142063656,
					3.92586483754593
				],
				[
					6.424112757065814,
					3.92586483754593
				],
				[
					6.424112757065814,
					3.5689606080394185
				],
				[
					7.137921216079121,
					3.21206999303719
				],
				[
					7.494811831081279,
					3.21206999303719
				],
				[
					8.208593061085594,
					2.4982751485284496
				],
				[
					8.208593061085594,
					2.141384533526221
				],
				[
					8.565483676087752,
					2.141384533526221
				],
				[
					8.565483676087752,
					1.4275896890174806
				],
				[
					8.565483676087752,
					1.0706990740152378
				],
				[
					9.279292135101059,
					1.0706990740152378
				],
				[
					9.279292135101059,
					1.0706990740152378
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 158,
			"versionNonce": 853545459,
			"isDeleted": false,
			"id": "FJKEY_vLLDzcFROZJjxWN",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2235.0412326395485,
			"y": -69.76544201343174,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 16.774103966181883,
			"height": 12.49136212813795,
			"seed": 72796511,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.7137812300047699,
					1.0706990740152378
				],
				[
					-1.0706718450069275,
					1.0706990740152378
				],
				[
					-1.0706718450069275,
					1.4275896890174806
				],
				[
					-1.4275896890176227,
					2.1413845335262067
				],
				[
					-2.141370919021938,
					2.4982751485284496
				],
				[
					-2.49826153402455,
					2.8551793780349612
				],
				[
					-3.212069993037403,
					3.5689606080394185
				],
				[
					-3.5689606080395606,
					3.92586483754593
				],
				[
					-4.282741838043876,
					4.996550297056899
				],
				[
					-4.639632453046488,
					4.996550297056899
				],
				[
					-4.996550297057183,
					5.710345141565625
				],
				[
					-5.7103315270614985,
					6.067235756567868
				],
				[
					-6.781030601076964,
					6.42413998607438
				],
				[
					-7.137921216079121,
					7.494825445585349
				],
				[
					-8.208593061085594,
					8.208620290094075
				],
				[
					-8.565510905096744,
					8.565510905096318
				],
				[
					-9.636182750103217,
					9.279305749605044
				],
				[
					-10.34999120911607,
					9.636196364607287
				],
				[
					-10.34999120911607,
					9.993100594113798
				],
				[
					-10.706881824118682,
					9.993100594113798
				],
				[
					-11.420663054122997,
					9.993100594113798
				],
				[
					-11.420663054122997,
					10.706881824118256
				],
				[
					-11.777553669125155,
					10.706881824118256
				],
				[
					-12.13447151313585,
					10.706881824118256
				],
				[
					-12.84825274314062,
					10.706881824118256
				],
				[
					-13.205143358142777,
					11.063786053624767
				],
				[
					-13.91895181715563,
					11.063786053624767
				],
				[
					-14.275842432157788,
					11.063786053624767
				],
				[
					-14.632733047159945,
					11.777580898133493
				],
				[
					-15.346514277164715,
					11.777580898133493
				],
				[
					-15.70343212117541,
					11.777580898133493
				],
				[
					-16.417213351179726,
					12.134471513135736
				],
				[
					-16.417213351179726,
					12.49136212813795
				],
				[
					-16.774103966181883,
					12.49136212813795
				],
				[
					-16.774103966181883,
					12.49136212813795
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 142,
			"versionNonce": 2019064509,
			"isDeleted": false,
			"id": "AyTsjbnaG1owc8JaRnBfA",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2253.956734753761,
			"y": -70.4792232434362,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 0,
			"height": 10.706881824118256,
			"seed": 1150748689,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.7137812300044573
				],
				[
					0,
					1.070685459510969
				],
				[
					0,
					1.784480304019695
				],
				[
					0,
					2.141370919021938
				],
				[
					0,
					3.212056378532907
				],
				[
					0,
					3.5689606080394185
				],
				[
					0,
					4.282741838043876
				],
				[
					0,
					4.639646067550387
				],
				[
					0,
					5.3534409120591135
				],
				[
					0,
					5.710331527061356
				],
				[
					0,
					6.067222142063571
				],
				[
					0,
					6.781016986572325
				],
				[
					0,
					7.137921216078837
				],
				[
					0,
					7.851702446083294
				],
				[
					0,
					8.208606675589806
				],
				[
					0,
					8.922401520098532
				],
				[
					0,
					9.279292135100775
				],
				[
					0,
					9.63618275010299
				],
				[
					0,
					10.349977594611744
				],
				[
					0,
					10.706881824118256
				],
				[
					0,
					10.706881824118256
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 149,
			"versionNonce": 865033107,
			"isDeleted": false,
			"id": "ByYdAuaeYYQxEI4rTOcYT",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2248.2464032266994,
			"y": -63.34130202735736,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 12.491362128138007,
			"height": 4.282741838043876,
			"seed": 1700524849,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3568906150021576,
					0
				],
				[
					0.7137812300043151,
					0
				],
				[
					1.4275624600086303,
					0.7137812300044573
				],
				[
					1.7844803040197803,
					1.070685459510969
				],
				[
					1.7844803040197803,
					1.784480304019695
				],
				[
					2.141370919021938,
					1.784480304019695
				],
				[
					2.141370919021938,
					2.141370919021938
				],
				[
					2.855152149026253,
					2.141370919021938
				],
				[
					2.855152149026253,
					2.4982615340241523
				],
				[
					3.2120427640284106,
					2.4982615340241523
				],
				[
					3.2120427640284106,
					3.212056378532907
				],
				[
					3.925851223041718,
					3.212056378532907
				],
				[
					3.925851223041718,
					3.5689606080394185
				],
				[
					4.282741838043876,
					4.282741838043876
				],
				[
					4.996523068048191,
					4.282741838043876
				],
				[
					5.353440912058886,
					4.282741838043876
				],
				[
					5.7103315270614985,
					4.282741838043876
				],
				[
					6.424112757065814,
					3.925851223041633
				],
				[
					7.494811831080824,
					3.925851223041633
				],
				[
					8.208593061085594,
					2.855165763530664
				],
				[
					9.279292135100604,
					2.855165763530664
				],
				[
					9.993073365105374,
					2.4982615340241523
				],
				[
					11.063772439120385,
					2.141370919021938
				],
				[
					11.420663054122542,
					1.4275760745131834
				],
				[
					11.7775536691247,
					1.4275760745131834
				],
				[
					11.7775536691247,
					1.070685459510969
				],
				[
					12.491362128138007,
					1.070685459510969
				],
				[
					12.491362128138007,
					1.070685459510969
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 151,
			"versionNonce": 341056285,
			"isDeleted": false,
			"id": "H4VtYNLsAsDtx_brR75W8",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2289.2894502191525,
			"y": -72.26370354745592,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 1.0706718450069275,
			"height": 14.989623662162131,
			"seed": 1868715889,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.35689061500224284
				],
				[
					0,
					0.7137812300044573
				],
				[
					0,
					1.070685459510969
				],
				[
					0,
					1.7844803040197235
				],
				[
					0,
					2.141370919021938
				],
				[
					0,
					2.8551657635306924
				],
				[
					0,
					3.212056378532907
				],
				[
					0,
					3.9258512230416613
				],
				[
					0,
					4.282741838043876
				],
				[
					0,
					5.353440912059142
				],
				[
					0,
					5.710331527061356
				],
				[
					0,
					6.781016986572325
				],
				[
					0,
					7.851702446083294
				],
				[
					0,
					8.208606675589806
				],
				[
					0,
					8.92240152009856
				],
				[
					0,
					9.279292135100775
				],
				[
					0,
					9.99308697960953
				],
				[
					0,
					10.349977594611744
				],
				[
					0,
					10.706881824118256
				],
				[
					0,
					11.420663054122713
				],
				[
					0,
					11.777567283629224
				],
				[
					0,
					12.491362128137979
				],
				[
					0,
					12.848252743140193
				],
				[
					0,
					13.562047587648948
				],
				[
					0.3568906150021576,
					13.562047587648948
				],
				[
					0.3568906150021576,
					13.918938202651162
				],
				[
					0.3568906150021576,
					14.275842432157674
				],
				[
					0.3568906150021576,
					14.989623662162131
				],
				[
					1.0706718450069275,
					14.989623662162131
				],
				[
					1.0706718450069275,
					14.989623662162131
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 150,
			"versionNonce": 518287667,
			"isDeleted": false,
			"id": "JG3DFcbu_Y9ph8R6MrLtK",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2283.9360093070936,
			"y": -60.12924564882445,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 11.420663054122542,
			"height": 3.212056378532907,
			"seed": 1576751985,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.35689061500224284
				],
				[
					0.7137812300043151,
					-0.35689061500224284
				],
				[
					1.0706718450064727,
					-0.35689061500224284
				],
				[
					1.7844803040197803,
					-0.35689061500224284
				],
				[
					1.7844803040197803,
					0.3569042295065117
				],
				[
					2.141370919021938,
					0.3569042295065117
				],
				[
					2.855152149026253,
					0.7137948445087261
				],
				[
					2.855152149026253,
					1.4275896890174806
				],
				[
					3.2120427640284106,
					1.4275896890174806
				],
				[
					3.568960608039106,
					1.784480304019695
				],
				[
					4.282741838043876,
					1.784480304019695
				],
				[
					4.282741838043876,
					2.1413845335262067
				],
				[
					4.639632453046033,
					2.1413845335262067
				],
				[
					4.639632453046033,
					2.855165763530664
				],
				[
					5.353440912058886,
					2.855165763530664
				],
				[
					5.710331527061044,
					2.855165763530664
				],
				[
					6.424112757065814,
					2.855165763530664
				],
				[
					6.781003372067971,
					2.855165763530664
				],
				[
					7.1379212160786665,
					2.855165763530664
				],
				[
					7.851702446082982,
					2.4982751485284496
				],
				[
					8.208593061085594,
					2.4982751485284496
				],
				[
					8.922401520098447,
					2.1413845335262067
				],
				[
					9.279292135100604,
					1.784480304019695
				],
				[
					9.636182750102762,
					1.070685459510969
				],
				[
					10.349963980107532,
					1.070685459510969
				],
				[
					10.706881824118227,
					0.7137948445087261
				],
				[
					11.420663054122542,
					0
				],
				[
					11.420663054122542,
					-0.35689061500224284
				],
				[
					11.420663054122542,
					-0.35689061500224284
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 142,
			"versionNonce": 79474557,
			"isDeleted": false,
			"id": "CgOwU8Uk2KBqLOKPHPsbk",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2261.0946559698396,
			"y": -68.33785232441426,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 16.060322736177568,
			"height": 11.420676668626982,
			"seed": 1694742001,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.0706990740154652,
					0.7137948445087261
				],
				[
					-1.7844803040197803,
					0.7137948445087261
				],
				[
					-2.141370919021938,
					1.784480304019695
				],
				[
					-3.212069993037403,
					2.141370919021938
				],
				[
					-3.5689606080395606,
					2.855165763530664
				],
				[
					-5.353440912059341,
					3.2120699930371757
				],
				[
					-6.424139986074351,
					4.282755452548145
				],
				[
					-6.781030601076509,
					4.282755452548145
				],
				[
					-7.851729675091974,
					5.3534409120591135
				],
				[
					-8.922401520098447,
					5.710331527061356
				],
				[
					-9.636209979111754,
					6.781030601076594
				],
				[
					-11.420690283131535,
					7.851716060587563
				],
				[
					-11.777580898133692,
					7.851716060587563
				],
				[
					-12.491362128138007,
					8.208606675589806
				],
				[
					-13.91895181715563,
					9.636196364607287
				],
				[
					-14.275842432157788,
					9.636196364607287
				],
				[
					-14.98965089117064,
					10.349991209116013
				],
				[
					-14.98965089117064,
					10.706881824118256
				],
				[
					-15.346541506172798,
					10.706881824118256
				],
				[
					-15.346541506172798,
					11.420676668626982
				],
				[
					-16.060322736177568,
					11.420676668626982
				],
				[
					-16.060322736177568,
					11.420676668626982
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 170,
			"versionNonce": 910545619,
			"isDeleted": false,
			"id": "gVUULf7Oqr35hT7zrQAfM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2198.994735944152,
			"y": -74.76197869598437,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 22.484462722251465,
			"height": 7.494825445585349,
			"seed": 651380127,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.3569042295065117
				],
				[
					0.7137812300043151,
					-0.3569042295065117
				],
				[
					1.0706990740150104,
					-1.070685459510969
				],
				[
					1.7844803040193256,
					-1.070685459510969
				],
				[
					2.141370919021938,
					-1.4275896890174806
				],
				[
					2.8551793780347907,
					-2.1413845335262067
				],
				[
					3.2120699930369483,
					-2.1413845335262067
				],
				[
					3.568960608039106,
					-2.1413845335262067
				],
				[
					4.282741838043876,
					-2.4982751485284496
				],
				[
					4.639659682054571,
					-2.855165763530664
				],
				[
					5.710331527061044,
					-2.855165763530664
				],
				[
					6.424139986074351,
					-3.5689606080394185
				],
				[
					6.781030601076509,
					-3.5689606080394185
				],
				[
					7.1379212160786665,
					-3.92586483754593
				],
				[
					7.851702446082982,
					-4.639646067550387
				],
				[
					8.208620290093677,
					-4.639646067550387
				],
				[
					8.922401520098447,
					-4.996550297056899
				],
				[
					9.279292135100604,
					-5.710345141565625
				],
				[
					9.636182750102762,
					-5.710345141565625
				],
				[
					10.349991209115615,
					-6.067235756567868
				],
				[
					10.706881824118227,
					-6.4241263715700825
				],
				[
					11.420663054122542,
					-6.4241263715700825
				],
				[
					11.777580898133237,
					-6.4241263715700825
				],
				[
					12.491362128138007,
					-7.137921216078837
				],
				[
					12.848252743140165,
					-7.137921216078837
				],
				[
					13.205143358142323,
					-7.137921216078837
				],
				[
					13.918951817155175,
					-7.137921216078837
				],
				[
					14.275842432157333,
					-7.494825445585349
				],
				[
					14.989623662162103,
					-7.494825445585349
				],
				[
					16.060322736177113,
					-7.494825445585349
				],
				[
					16.41721335117927,
					-7.494825445585349
				],
				[
					17.487912425194736,
					-7.494825445585349
				],
				[
					17.844803040196894,
					-7.494825445585349
				],
				[
					18.55858427020121,
					-7.494825445585349
				],
				[
					18.915502114211904,
					-7.494825445585349
				],
				[
					19.629283344216674,
					-7.494825445585349
				],
				[
					19.98617395921883,
					-7.494825445585349
				],
				[
					20.34306457422099,
					-7.494825445585349
				],
				[
					21.056873033233842,
					-7.494825445585349
				],
				[
					21.413763648236454,
					-7.494825445585349
				],
				[
					21.413763648236454,
					-6.781030601076594
				],
				[
					22.12754487824077,
					-6.781030601076594
				],
				[
					22.12754487824077,
					-6.4241263715700825
				],
				[
					22.484462722251465,
					-6.4241263715700825
				],
				[
					22.484462722251465,
					-6.067235756567868
				],
				[
					22.484462722251465,
					-5.3534409120591135
				],
				[
					22.484462722251465,
					-4.996550297056899
				],
				[
					22.484462722251465,
					-4.282755452548145
				],
				[
					22.484462722251465,
					-3.92586483754593
				],
				[
					22.484462722251465,
					-3.2120699930371757
				],
				[
					22.484462722251465,
					-3.2120699930371757
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 147,
			"versionNonce": 399751133,
			"isDeleted": false,
			"id": "xlo6CRXLvrj7QN7964bGk",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2214.698168065327,
			"y": -77.26025384451282,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 9.279292135100604,
			"height": 3.5689606080394185,
			"seed": 1741244479,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.3568906150022144
				],
				[
					0.3568906150021576,
					-0.3568906150022144
				],
				[
					0.7137812300043151,
					-0.3568906150022144
				],
				[
					1.0706718450069275,
					-0.3568906150022144
				],
				[
					1.0706718450069275,
					0
				],
				[
					1.7844803040197803,
					0
				],
				[
					2.141370919021938,
					0.7137948445087545
				],
				[
					2.855152149026253,
					0.7137948445087545
				],
				[
					2.855152149026253,
					1.070685459510969
				],
				[
					3.2120699930369483,
					1.070685459510969
				],
				[
					3.925851223041718,
					1.7844803040197235
				],
				[
					4.282741838043876,
					1.7844803040197235
				],
				[
					4.282741838043876,
					2.141370919021938
				],
				[
					4.639632453046033,
					2.141370919021938
				],
				[
					5.353440912058886,
					2.141370919021938
				],
				[
					5.7103315270614985,
					2.141370919021938
				],
				[
					6.424112757065814,
					2.141370919021938
				],
				[
					6.781030601076509,
					2.141370919021938
				],
				[
					7.1379212160786665,
					2.141370919021938
				],
				[
					7.851702446083436,
					1.4275896890174806
				],
				[
					7.851702446083436,
					1.070685459510969
				],
				[
					8.208593061085594,
					0.35689061500224284
				],
				[
					8.922401520098447,
					0
				],
				[
					8.922401520098447,
					-0.3568906150022144
				],
				[
					9.279292135100604,
					-0.3568906150022144
				],
				[
					9.279292135100604,
					-1.070685459510969
				],
				[
					9.279292135100604,
					-1.4275896890174806
				],
				[
					9.279292135100604,
					-1.4275896890174806
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 168,
			"versionNonce": 1246363763,
			"isDeleted": false,
			"id": "PJ9RWbddBxma6FPWGRiox",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2227.189530193465,
			"y": -77.26025384451282,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 22.12754487824077,
			"height": 8.92240152009856,
			"seed": 1565802495,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.3568906150022144
				],
				[
					0,
					-1.070685459510969
				],
				[
					0.3568906150021576,
					-1.070685459510969
				],
				[
					1.0706718450064727,
					-1.4275896890174806
				],
				[
					1.4275896890176227,
					-1.4275896890174806
				],
				[
					1.7844803040197803,
					-2.141370919021938
				],
				[
					2.4982615340240955,
					-2.141370919021938
				],
				[
					3.5689606080395606,
					-2.141370919021938
				],
				[
					3.925851223041718,
					-2.4982751485284496
				],
				[
					4.282741838043876,
					-2.4982751485284496
				],
				[
					4.996550297056729,
					-3.2120699930371757
				],
				[
					5.353440912058886,
					-3.2120699930371757
				],
				[
					6.067222142063656,
					-3.2120699930371757
				],
				[
					6.424112757065814,
					-3.2120699930371757
				],
				[
					7.494811831081279,
					-3.5689606080394185
				],
				[
					7.851702446083436,
					-3.5689606080394185
				],
				[
					9.636182750103217,
					-3.5689606080394185
				],
				[
					9.993073365105374,
					-3.5689606080394185
				],
				[
					10.706881824118227,
					-3.5689606080394185
				],
				[
					11.420663054122542,
					-3.5689606080394185
				],
				[
					12.13447151313585,
					-3.5689606080394185
				],
				[
					13.205143358142323,
					-3.5689606080394185
				],
				[
					13.56203397314448,
					-3.5689606080394185
				],
				[
					14.275842432157788,
					-3.5689606080394185
				],
				[
					14.632733047159945,
					-3.5689606080394185
				],
				[
					14.989623662162103,
					-3.5689606080394185
				],
				[
					15.703432121174956,
					-3.5689606080394185
				],
				[
					15.703432121174956,
					-2.855165763530664
				],
				[
					16.060322736177113,
					-2.855165763530664
				],
				[
					16.060322736177113,
					-2.4982751485284496
				],
				[
					17.13099458118404,
					-1.784480304019695
				],
				[
					17.13099458118404,
					-1.4275896890174806
				],
				[
					17.487912425194736,
					-1.4275896890174806
				],
				[
					17.487912425194736,
					-0.7137948445087261
				],
				[
					18.20169365519905,
					-0.3568906150022144
				],
				[
					18.558584270201663,
					0
				],
				[
					18.558584270201663,
					0.7137948445087545
				],
				[
					19.272392729214516,
					1.070685459510969
				],
				[
					19.629283344216674,
					1.7844803040197235
				],
				[
					19.629283344216674,
					2.141370919021938
				],
				[
					19.629283344216674,
					2.8551657635306924
				],
				[
					20.34306457422099,
					2.8551657635306924
				],
				[
					20.34306457422099,
					3.212069993037204
				],
				[
					20.6999551892236,
					3.5689606080394185
				],
				[
					21.056873033234297,
					4.282755452548173
				],
				[
					21.77065426323861,
					4.282755452548173
				],
				[
					21.77065426323861,
					4.639646067550387
				],
				[
					22.12754487824077,
					5.353440912059142
				],
				[
					22.12754487824077,
					5.353440912059142
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 150,
			"versionNonce": 1470805053,
			"isDeleted": false,
			"id": "TJ8bCQzmIwcx8MJ2b9QfM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2243.249852929642,
			"y": -75.83266415549534,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 9.279292135101059,
			"height": 8.208606675589806,
			"seed": 791630431,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7137812300047699,
					0
				],
				[
					0.7137812300047699,
					0.35689061500224284
				],
				[
					1.0706718450069275,
					0.7137812300044573
				],
				[
					1.4275896890176227,
					0.7137812300044573
				],
				[
					1.4275896890176227,
					1.4275760745132118
				],
				[
					2.141370919021938,
					1.4275760745132118
				],
				[
					2.141370919021938,
					1.7844803040197235
				],
				[
					3.212069993037403,
					1.7844803040197235
				],
				[
					3.212069993037403,
					2.141370919021938
				],
				[
					3.5689606080395606,
					2.141370919021938
				],
				[
					4.282741838043876,
					2.8551657635306924
				],
				[
					4.639632453046488,
					2.8551657635306924
				],
				[
					4.996550297057183,
					2.8551657635306924
				],
				[
					5.7103315270614985,
					2.8551657635306924
				],
				[
					6.067222142063656,
					2.8551657635306924
				],
				[
					6.781030601076964,
					2.4982615340241807
				],
				[
					6.781030601076964,
					2.141370919021938
				],
				[
					7.137921216079121,
					1.7844803040197235
				],
				[
					7.851702446083436,
					1.070685459510969
				],
				[
					7.851702446083436,
					0.7137812300044573
				],
				[
					7.851702446083436,
					0
				],
				[
					8.208593061085594,
					-1.0706990740152378
				],
				[
					8.208593061085594,
					-1.4275896890174806
				],
				[
					8.565510905096744,
					-2.4982751485284496
				],
				[
					8.565510905096744,
					-2.8551793780349612
				],
				[
					8.565510905096744,
					-3.5689606080394185
				],
				[
					9.279292135101059,
					-3.92586483754593
				],
				[
					9.279292135101059,
					-4.639659682054656
				],
				[
					9.279292135101059,
					-4.996550297056899
				],
				[
					9.279292135101059,
					-5.3534409120591135
				],
				[
					9.279292135101059,
					-5.3534409120591135
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 180,
			"versionNonce": 1421310483,
			"isDeleted": false,
			"id": "mBYR72LgBOgTVvqj3Lfwu",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2253.5998441387583,
			"y": -77.97404868902154,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 28.908575479317733,
			"height": 8.92240152009856,
			"seed": 1293349503,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.427562460009085,
					-0.35689061500224284
				],
				[
					1.7844803040197803,
					-0.35689061500224284
				],
				[
					2.49826153402455,
					-0.7137948445087545
				],
				[
					2.8551521490267078,
					-0.7137948445087545
				],
				[
					3.5689606080395606,
					-1.4275760745132118
				],
				[
					3.925851223041718,
					-1.4275760745132118
				],
				[
					4.282741838043876,
					-1.4275760745132118
				],
				[
					4.996523068048646,
					-1.7844803040197235
				],
				[
					5.353440912059341,
					-1.7844803040197235
				],
				[
					6.067222142063656,
					-2.4982751485284496
				],
				[
					6.424112757065814,
					-2.4982751485284496
				],
				[
					7.137921216079121,
					-2.4982751485284496
				],
				[
					7.494811831081279,
					-2.8551657635306924
				],
				[
					7.851702446083436,
					-2.8551657635306924
				],
				[
					8.565483676088206,
					-2.8551657635306924
				],
				[
					8.922401520098902,
					-3.212056378532907
				],
				[
					9.636182750103217,
					-3.212056378532907
				],
				[
					9.993073365105374,
					-3.212056378532907
				],
				[
					10.706881824118227,
					-3.9258512230416613
				],
				[
					11.420663054122997,
					-3.9258512230416613
				],
				[
					12.134444284127312,
					-3.9258512230416613
				],
				[
					12.491362128138007,
					-3.9258512230416613
				],
				[
					13.205143358142777,
					-3.9258512230416613
				],
				[
					13.562033973144935,
					-3.9258512230416613
				],
				[
					13.918924588147092,
					-3.9258512230416613
				],
				[
					14.989623662162103,
					-3.9258512230416613
				],
				[
					15.703404892166873,
					-3.9258512230416613
				],
				[
					16.060322736177568,
					-3.5689606080394185
				],
				[
					16.774103966181883,
					-3.5689606080394185
				],
				[
					16.774103966181883,
					-3.212056378532907
				],
				[
					17.13099458118404,
					-3.212056378532907
				],
				[
					17.487885196186653,
					-2.8551657635306924
				],
				[
					18.201693655199506,
					-2.8551657635306924
				],
				[
					18.558584270201663,
					-2.141370919021938
				],
				[
					19.27236550020598,
					-2.141370919021938
				],
				[
					19.62928334421713,
					-1.7844803040197235
				],
				[
					20.343064574221444,
					-1.070685459510969
				],
				[
					20.6999551892236,
					-0.7137948445087545
				],
				[
					21.770654263239066,
					0
				],
				[
					22.127544878241224,
					0
				],
				[
					22.84132610824554,
					0.3569042295065117
				],
				[
					22.84132610824554,
					0.7137948445087261
				],
				[
					23.198243952256234,
					0.7137948445087261
				],
				[
					23.912025182261004,
					1.4275896890174806
				],
				[
					24.268915797263162,
					1.784480304019695
				],
				[
					24.62580641226532,
					1.784480304019695
				],
				[
					24.62580641226532,
					2.4982751485284496
				],
				[
					25.339614871278172,
					2.4982751485284496
				],
				[
					25.339614871278172,
					2.855165763530664
				],
				[
					25.696505486280785,
					2.855165763530664
				],
				[
					26.4102867162851,
					2.855165763530664
				],
				[
					26.4102867162851,
					3.5689606080394185
				],
				[
					26.767204560295795,
					3.5689606080394185
				],
				[
					26.767204560295795,
					3.92586483754593
				],
				[
					27.124095175297953,
					3.92586483754593
				],
				[
					27.837876405302723,
					3.92586483754593
				],
				[
					27.837876405302723,
					4.282755452548145
				],
				[
					28.19476702030488,
					4.282755452548145
				],
				[
					28.908575479317733,
					4.282755452548145
				],
				[
					28.908575479317733,
					4.996550297056899
				],
				[
					28.908575479317733,
					4.996550297056899
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 152,
			"versionNonce": 270738589,
			"isDeleted": false,
			"id": "GRakNokDeg7PAxq0E-aUo",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2275.013607786995,
			"y": -71.19301808794495,
			"strokeColor": "#f08c00",
			"backgroundColor": "transparent",
			"width": 8.922401520098447,
			"height": 8.565497290592049,
			"seed": 338861663,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3568906150021576,
					0
				],
				[
					0.7137812300043151,
					0
				],
				[
					1.4275624600086303,
					0
				],
				[
					1.7844803040193256,
					0
				],
				[
					2.4982615340240955,
					0
				],
				[
					2.855152149026253,
					0
				],
				[
					3.2120427640284106,
					0
				],
				[
					3.9258512230412634,
					0
				],
				[
					4.282741838043876,
					0
				],
				[
					4.282741838043876,
					0.35689061500224284
				],
				[
					4.996523068048191,
					0.35689061500224284
				],
				[
					5.353440912058886,
					0.35689061500224284
				],
				[
					5.710331527061044,
					0.35689061500224284
				],
				[
					6.424112757065814,
					0.35689061500224284
				],
				[
					6.781003372067971,
					0.35689061500224284
				],
				[
					7.494811831080824,
					0.35689061500224284
				],
				[
					7.494811831080824,
					0
				],
				[
					7.851702446082982,
					-0.3569042295065117
				],
				[
					7.851702446082982,
					-1.070685459510969
				],
				[
					8.565483676087752,
					-1.4275896890174806
				],
				[
					8.565483676087752,
					-2.1413845335262067
				],
				[
					8.565483676087752,
					-2.4982751485284496
				],
				[
					8.565483676087752,
					-3.5689606080394185
				],
				[
					8.565483676087752,
					-3.92586483754593
				],
				[
					8.922401520098447,
					-4.639646067550387
				],
				[
					8.922401520098447,
					-4.996550297056899
				],
				[
					8.922401520098447,
					-5.710345141565625
				],
				[
					8.922401520098447,
					-6.067235756567868
				],
				[
					8.922401520098447,
					-6.4241263715700825
				],
				[
					8.922401520098447,
					-7.137921216078837
				],
				[
					8.922401520098447,
					-7.494825445585349
				],
				[
					8.922401520098447,
					-8.208606675589806
				],
				[
					8.922401520098447,
					-8.208606675589806
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 135,
			"versionNonce": 1384431539,
			"isDeleted": false,
			"id": "I3q8xDtir5ImcmtRaoD6S",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2290.0032314491573,
			"y": -130.43777235010185,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 15.346541506173253,
			"height": 7.851716060587577,
			"seed": 887874737,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-1.0706990740154652,
					0
				],
				[
					-1.4275896890176227,
					0
				],
				[
					-2.49826153402455,
					0.7137948445087403
				],
				[
					-4.639659682055026,
					1.7844803040197093
				],
				[
					-4.996550297057183,
					1.7844803040197093
				],
				[
					-6.067222142063656,
					2.8551793780349612
				],
				[
					-8.208620290094132,
					3.5689606080394185
				],
				[
					-9.279292135101059,
					4.282755452548159
				],
				[
					-11.06377243912084,
					5.353440912059128
				],
				[
					-13.205143358142777,
					6.42413998607438
				],
				[
					-13.205143358142777,
					6.781030601076608
				],
				[
					-14.275842432157788,
					7.137921216078837
				],
				[
					-14.632733047159945,
					7.137921216078837
				],
				[
					-15.346541506173253,
					7.137921216078837
				],
				[
					-15.346541506173253,
					7.851716060587577
				],
				[
					-15.346541506173253,
					7.851716060587577
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 136,
			"versionNonce": 351176957,
			"isDeleted": false,
			"id": "FL8g8ngunFzTmGtp2Uh29",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2276.441170247004,
			"y": -34.075822318533284,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 19.986201188227824,
			"height": 0.713808459012995,
			"seed": 1319973151,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7138084590133076,
					0
				],
				[
					1.0706990740154652,
					0
				],
				[
					2.498288763032633,
					0
				],
				[
					4.2827690670524134,
					0
				],
				[
					5.710358756070036,
					0
				],
				[
					7.137921216079121,
					0
				],
				[
					9.279319364109597,
					0
				],
				[
					9.636209979111754,
					0
				],
				[
					11.420690283131535,
					0
				],
				[
					13.20517058715086,
					0
				],
				[
					16.417240580188263,
					0
				],
				[
					16.77413119519042,
					0
				],
				[
					17.84480304019735,
					0
				],
				[
					18.91550211421236,
					-0.713808459012995
				],
				[
					19.272392729214516,
					-0.713808459012995
				],
				[
					19.986201188227824,
					-0.713808459012995
				],
				[
					19.986201188227824,
					-0.713808459012995
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 187,
			"versionNonce": 1574457683,
			"isDeleted": false,
			"id": "9uT5R9qQ2pcGo5JXHbTnD",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2297.498043280238,
			"y": -31.22067016950686,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 111.7084779232373,
			"height": 14.275842432157674,
			"seed": 1049215377,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.3569178440107805
				],
				[
					0,
					1.0706990740152378
				],
				[
					0,
					1.4275896890174806
				],
				[
					0,
					2.1413981480304756
				],
				[
					0.3568906150021576,
					2.4982887630327184
				],
				[
					1.0706990740154652,
					2.4982887630327184
				],
				[
					1.4275896890176227,
					3.2120699930371757
				],
				[
					2.498288763032633,
					3.2120699930371757
				],
				[
					3.5689606080395606,
					3.2120699930371757
				],
				[
					4.639659682054571,
					3.2120699930371757
				],
				[
					7.137921216079121,
					3.5689606080394185
				],
				[
					11.777580898133692,
					3.5689606080394185
				],
				[
					16.060322736177568,
					3.5689606080394185
				],
				[
					18.91550211421236,
					3.5689606080394185
				],
				[
					27.124095175297953,
					3.5689606080394185
				],
				[
					37.117195769411865,
					3.5689606080394185
				],
				[
					46.03959728951031,
					3.5689606080394185
				],
				[
					56.03269788362422,
					3.5689606080394185
				],
				[
					67.09647032274461,
					4.2827690670524134
				],
				[
					78.16024276186499,
					4.2827690670524134
				],
				[
					91.00849550500516,
					4.996550297056899
				],
				[
					98.8601979510886,
					4.996550297056899
				],
				[
					105.28433793716295,
					4.996550297056899
				],
				[
					109.56707977520682,
					4.996550297056899
				],
				[
					110.99469669323298,
					4.996550297056899
				],
				[
					111.7084779232373,
					4.996550297056899
				],
				[
					111.3515600792266,
					4.996550297056899
				],
				[
					111.3515600792266,
					4.2827690670524134
				],
				[
					110.99469669323298,
					4.2827690670524134
				],
				[
					110.63777884922183,
					4.2827690670524134
				],
				[
					109.92399761921752,
					4.2827690670524134
				],
				[
					109.56707977520682,
					4.2827690670524134
				],
				[
					108.8532985452025,
					4.2827690670524134
				],
				[
					108.49643515920889,
					4.2827690670524134
				],
				[
					107.42573608519342,
					3.925878452050199
				],
				[
					107.06881824118273,
					3.925878452050199
				],
				[
					105.99811916716726,
					3.2120699930371757
				],
				[
					104.57055670715863,
					2.855179378034933
				],
				[
					103.85677547715386,
					2.855179378034933
				],
				[
					103.49985763314317,
					2.855179378034933
				],
				[
					102.78607640313885,
					2.4982887630327184
				],
				[
					101.71537732912338,
					2.4982887630327184
				],
				[
					101.35851394312976,
					1.784480304019695
				],
				[
					101.00159609911907,
					1.784480304019695
				],
				[
					100.28781486911475,
					1.784480304019695
				],
				[
					99.93089702510406,
					1.784480304019695
				],
				[
					99.21711579509929,
					1.784480304019695
				],
				[
					98.8601979510886,
					1.4275896890174806
				],
				[
					98.14641672108428,
					1.4275896890174806
				],
				[
					97.7895533350902,
					1.4275896890174806
				],
				[
					97.43263549107951,
					1.4275896890174806
				],
				[
					96.7188542610752,
					1.4275896890174806
				],
				[
					96.3619364170645,
					1.4275896890174806
				],
				[
					95.64815518705973,
					1.4275896890174806
				],
				[
					95.29123734304903,
					1.4275896890174806
				],
				[
					95.29123734304903,
					2.1413981480304756
				],
				[
					95.29123734304903,
					2.4982887630327184
				],
				[
					95.29123734304903,
					3.5689606080394185
				],
				[
					95.29123734304903,
					3.925878452050199
				],
				[
					95.29123734304903,
					4.996550297056899
				],
				[
					95.29123734304903,
					6.067249371072137
				],
				[
					95.29123734304903,
					7.137921216078837
				],
				[
					95.29123734304903,
					8.208620290094075
				],
				[
					95.29123734304903,
					8.922401520098532
				],
				[
					95.29123734304903,
					9.99310059411377
				],
				[
					95.29123734304903,
					11.063799668129036
				],
				[
					95.29123734304903,
					12.134471513135736
				],
				[
					95.29123734304903,
					12.49136212813795
				],
				[
					95.29123734304903,
					13.205170587150974
				],
				[
					95.29123734304903,
					13.562061202153188
				],
				[
					95.29123734304903,
					14.275842432157674
				],
				[
					95.29123734304903,
					14.275842432157674
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 142,
			"versionNonce": 1200513373,
			"isDeleted": false,
			"id": "zjcc5xcnTG-oB2x0SHb9b",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2387.435866940237,
			"y": -20.870678960390848,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 10.70685459510969,
			"height": 3.9258512230416613,
			"seed": 240724049,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.0706718450064727,
					0
				],
				[
					1.4275624600086303,
					0
				],
				[
					1.7844803040197803,
					0
				],
				[
					2.4982615340240955,
					0.35689061500224284
				],
				[
					2.4982615340240955,
					0.7138084590130234
				],
				[
					2.855152149026253,
					0.7138084590130234
				],
				[
					2.855152149026253,
					1.4275896890174806
				],
				[
					3.568960608039106,
					1.7844803040197235
				],
				[
					3.925851223041718,
					1.7844803040197235
				],
				[
					3.925851223041718,
					2.141370919021938
				],
				[
					4.639632453046033,
					2.141370919021938
				],
				[
					4.639632453046033,
					2.8551793780349612
				],
				[
					4.996550297056729,
					2.8551793780349612
				],
				[
					4.996550297056729,
					3.2120699930371757
				],
				[
					5.3534136830503485,
					3.2120699930371757
				],
				[
					5.3534136830503485,
					3.9258512230416613
				],
				[
					6.067249371072194,
					3.9258512230416613
				],
				[
					6.424112757065814,
					3.5689606080394185
				],
				[
					7.137893987070129,
					3.2120699930371757
				],
				[
					7.494811831080824,
					2.4982887630327184
				],
				[
					7.851729675091519,
					2.141370919021938
				],
				[
					8.56551090509629,
					1.7844803040197235
				],
				[
					8.922374291089909,
					1.7844803040197235
				],
				[
					9.6362099791113,
					1.0706990740152378
				],
				[
					9.993073365105374,
					1.0706990740152378
				],
				[
					10.70685459510969,
					1.0706990740152378
				],
				[
					10.70685459510969,
					1.0706990740152378
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 132,
			"versionNonce": 134786803,
			"isDeleted": false,
			"id": "7NhOaQFl0NUIe7eE7X6RD",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2272.8722096389643,
			"y": -91.53609627667049,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 12.491362128138007,
			"height": 0,
			"seed": 1896043185,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.35691784401115,
					0
				],
				[
					0.7138084590133076,
					0
				],
				[
					1.7844803040197803,
					0
				],
				[
					3.925878452050256,
					0
				],
				[
					4.282769067052868,
					0
				],
				[
					5.710358756070036,
					0
				],
				[
					7.4948390600898165,
					0
				],
				[
					8.565510905096744,
					0
				],
				[
					8.922401520098902,
					0
				],
				[
					9.279319364109597,
					0
				],
				[
					9.993100594113912,
					0
				],
				[
					10.34999120911607,
					0
				],
				[
					11.063799668129377,
					0
				],
				[
					11.420690283131535,
					0
				],
				[
					12.13447151313585,
					0
				],
				[
					12.491362128138007,
					0
				],
				[
					12.491362128138007,
					0
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 303,
			"versionNonce": 1565797821,
			"isDeleted": false,
			"id": "T-3S7fC2m3GFFPsiCIAmp",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2280.723939314056,
			"y": -91.17920566166825,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 319.06509061177803,
			"height": 124.19982643687095,
			"seed": 1733360849,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.7137948445087261
				],
				[
					0,
					1.0706990740152378
				],
				[
					0,
					1.784480304019695
				],
				[
					0,
					2.1413845335262067
				],
				[
					0,
					2.8551793780349612
				],
				[
					0,
					3.2120699930371757
				],
				[
					0,
					3.5689606080394185
				],
				[
					0,
					4.282755452548145
				],
				[
					0,
					4.639659682054656
				],
				[
					0,
					5.3534409120591135
				],
				[
					0,
					4.996550297056899
				],
				[
					-0.7138084590128528,
					4.996550297056899
				],
				[
					-1.0706990740150104,
					4.639659682054656
				],
				[
					-1.7844803040197803,
					4.639659682054656
				],
				[
					-2.141370919021938,
					4.639659682054656
				],
				[
					-2.498288763032633,
					4.639659682054656
				],
				[
					-3.568960608039106,
					4.639659682054656
				],
				[
					-5.353440912058886,
					4.639659682054656
				],
				[
					-5.710331527061044,
					4.639659682054656
				],
				[
					-7.1379212160786665,
					4.639659682054656
				],
				[
					-9.279292135100604,
					5.3534409120591135
				],
				[
					-11.42069028313108,
					5.3534409120591135
				],
				[
					-17.487912425194736,
					5.3534409120591135
				],
				[
					-18.558611499209746,
					5.3534409120591135
				],
				[
					-25.339614871278172,
					5.3534409120591135
				],
				[
					-32.834453931367534,
					5.3534409120591135
				],
				[
					-38.54478545842903,
					5.3534409120591135
				],
				[
					-53.534409120591135,
					5.3534409120591135
				],
				[
					-57.460260343632854,
					6.067235756567868
				],
				[
					-68.52406001176178,
					6.067235756567868
				],
				[
					-84.58438274793934,
					6.781030601076594
				],
				[
					-102.07226794412554,
					8.565510905096318
				],
				[
					-115.63432914627856,
					9.279305749605044
				],
				[
					-123.12915459186434,
					9.993100594113798
				],
				[
					-140.61705340255457,
					11.420676668626982
				],
				[
					-154.5360052197102,
					13.205156972646705
				],
				[
					-165.95668188833724,
					14.632746661664186
				],
				[
					-183.80148492853414,
					16.774117580686124
				],
				[
					-194.50836675265236,
					18.201707269703604
				],
				[
					-198.07732736069192,
					18.201707269703604
				],
				[
					-207.35661949579253,
					18.91550211421233
				],
				[
					-215.20833555638046,
					19.9861875737233
				],
				[
					-216.9928158603998,
					19.9861875737233
				],
				[
					-221.63246192795032,
					19.9861875737233
				],
				[
					-224.1307370764789,
					19.9861875737233
				],
				[
					-225.20142253598988,
					19.9861875737233
				],
				[
					-225.55831315099203,
					19.9861875737233
				],
				[
					-226.27210799550085,
					19.9861875737233
				],
				[
					-226.62901222500705,
					19.9861875737233
				],
				[
					-226.62901222500705,
					20.699982418232054
				],
				[
					-226.62901222500705,
					21.056873033234268
				],
				[
					-227.34279345501182,
					22.127558492745237
				],
				[
					-227.69969768451847,
					23.555148181762718
				],
				[
					-228.41349252902705,
					24.625833641273687
				],
				[
					-228.7703831440292,
					26.41031394529341
				],
				[
					-228.7703831440292,
					26.767204560295625
				],
				[
					-229.84106860354018,
					29.265479708824074
				],
				[
					-230.1979728330466,
					31.40686424235031
				],
				[
					-230.1979728330466,
					31.763754857352524
				],
				[
					-230.91175406305115,
					33.90512577637446
				],
				[
					-231.26865829255757,
					34.26203000588097
				],
				[
					-231.62555571481198,
					37.83099061392039
				],
				[
					-231.62555571481198,
					40.32926576244884
				],
				[
					-231.62555571481198,
					42.113746066468565
				],
				[
					-231.62555571481198,
					44.612007600492745
				],
				[
					-231.62555571481198,
					44.96891182999923
				],
				[
					-231.62555571481198,
					46.39648790451244
				],
				[
					-231.62555571481198,
					49.60857151205391
				],
				[
					-231.62555571481198,
					51.74994243107585
				],
				[
					-231.62555571481198,
					52.106833046078066
				],
				[
					-231.62555571481198,
					56.03268426911973
				],
				[
					-231.62555571481198,
					59.2447542621569
				],
				[
					-231.62555571481198,
					61.38612518117887
				],
				[
					-231.62555571481198,
					63.88441394421159
				],
				[
					-231.62555571481198,
					64.95508578921829
				],
				[
					-231.62555571481198,
					66.73956609323798
				],
				[
					-231.26865829255757,
					68.16715578225546
				],
				[
					-231.26865829255757,
					68.5240463972577
				],
				[
					-230.554863448049,
					71.73611639029488
				],
				[
					-230.554863448049,
					72.80681546431012
				],
				[
					-230.554863448049,
					74.59129576832984
				],
				[
					-230.1979728330466,
					77.80333853235848
				],
				[
					-230.1979728330466,
					78.16025637636926
				],
				[
					-229.48417798853802,
					79.94473668038896
				],
				[
					-229.48417798853802,
					82.44299821441314
				],
				[
					-229.48417798853802,
					82.79988882941538
				],
				[
					-229.48417798853802,
					84.22747851843286
				],
				[
					-229.48417798853802,
					84.94125974843732
				],
				[
					-229.12727375903137,
					86.3688494374548
				],
				[
					-229.12727375903137,
					87.43954851147004
				],
				[
					-228.7703831440292,
					88.51022035647674
				],
				[
					-228.7703831440292,
					88.86713820048752
				],
				[
					-228.7703831440292,
					89.58091943049197
				],
				[
					-228.7703831440292,
					89.93781004549422
				],
				[
					-228.7703831440292,
					90.29470066049643
				],
				[
					-228.7703831440292,
					91.00850911950945
				],
				[
					-228.0565882995204,
					91.00850911950945
				],
				[
					-228.0565882995204,
					91.3653997345117
				],
				[
					-228.0565882995204,
					92.07918096451615
				],
				[
					-228.0565882995204,
					92.43609880852694
				],
				[
					-228.0565882995204,
					93.14988003853139
				],
				[
					-228.0565882995204,
					93.86366126853585
				],
				[
					-227.69969768451847,
					95.64814157255557
				],
				[
					-227.69969768451847,
					96.71884064657081
				],
				[
					-227.69969768451847,
					97.07573126157305
				],
				[
					-227.69969768451847,
					97.43262187657527
				],
				[
					-227.69969768451847,
					98.14643033558829
				],
				[
					-226.98590284000966,
					98.50332095059053
				],
				[
					-226.98590284000966,
					99.57402002460577
				],
				[
					-226.98590284000966,
					99.93091063960799
				],
				[
					-226.98590284000966,
					101.71539094362771
				],
				[
					-226.62901222500705,
					101.71539094362771
				],
				[
					-226.62901222500705,
					102.07228155862995
				],
				[
					-226.62901222500705,
					102.78606278863441
				],
				[
					-225.9152173804987,
					102.78606278863441
				],
				[
					-225.9152173804987,
					103.14298063264519
				],
				[
					-225.9152173804987,
					103.49987124764743
				],
				[
					-225.9152173804987,
					104.21365247765189
				],
				[
					-225.9152173804987,
					104.5705430926541
				],
				[
					-225.20142253598988,
					104.5705430926541
				],
				[
					-221.63246192795032,
					105.64124216666937
				],
				[
					-218.06350131991076,
					106.35502339667383
				],
				[
					-207.35661949579253,
					107.78261308569131
				],
				[
					-193.43766767863735,
					109.92398400471322
				],
				[
					-188.44113099608467,
					110.63779246372624
				],
				[
					-162.38772128029768,
					114.20675307176569
				],
				[
					-149.18256430765086,
					115.99123337578541
				],
				[
					-93.86367488303995,
					120.6308658288315
				],
				[
					-85.29816397794366,
					120.6308658288315
				],
				[
					-77.08954368784953,
					121.70156490284674
				],
				[
					-28.194794249312963,
					122.41534613285123
				],
				[
					-19.98617395921883,
					122.41534613285123
				],
				[
					19.272392729214516,
					122.41534613285123
				],
				[
					32.83442670235945,
					123.48604520686646
				],
				[
					61.74300218167673,
					124.19982643687095
				],
				[
					70.30851308677347,
					124.19982643687095
				],
				[
					84.22746490392865,
					124.19982643687095
				],
				[
					84.5843555189308,
					124.19982643687095
				],
				[
					85.65505459294627,
					124.19982643687095
				],
				[
					87.43953489696605,
					124.19982643687095
				],
				[
					87.0826442819639,
					123.84293582186868
				],
				[
					87.0826442819639,
					123.12915459186425
				],
				[
					85.65505459294627,
					122.77226397686198
				],
				[
					85.29816397794411,
					122.05845551784896
				],
				[
					84.5843555189308,
					122.05845551784896
				],
				[
					84.22746490392865,
					122.05845551784896
				],
				[
					83.51368367392433,
					122.05845551784896
				],
				[
					83.51368367392433,
					121.70156490284674
				],
				[
					83.15676582991364,
					121.70156490284674
				],
				[
					82.08609398490671,
					120.98778367284226
				],
				[
					81.01539491089125,
					120.6308658288315
				],
				[
					79.94472306588477,
					120.6308658288315
				],
				[
					79.94472306588477,
					120.27397521382929
				],
				[
					79.58780522187408,
					120.27397521382929
				],
				[
					79.23091460687192,
					119.5601939838248
				],
				[
					78.51713337686715,
					119.5601939838248
				],
				[
					78.51713337686715,
					119.20330336882259
				],
				[
					78.51713337686715,
					118.48949490980957
				],
				[
					78.87402399186931,
					118.13260429480735
				],
				[
					79.23091460687192,
					117.41882306480287
				],
				[
					79.23091460687192,
					117.06190522079211
				],
				[
					79.23091460687192,
					115.99123337578541
				],
				[
					79.23091460687192,
					114.92053430177012
				],
				[
					79.23091460687192,
					114.5636436867679
				],
				[
					79.23091460687192,
					114.20675307176569
				],
				[
					79.23091460687192,
					113.49294461275267
				],
				[
					79.23091460687192,
					113.13605399775045
				],
				[
					79.23091460687192,
					112.06538215274375
				],
				[
					79.23091460687192,
					111.35157369373073
				],
				[
					79.23091460687192,
					110.63779246372624
				],
				[
					79.23091460687192,
					109.92398400471322
				],
				[
					79.23091460687192,
					109.567093389711
				],
				[
					78.51713337686715,
					108.85331215970655
				],
				[
					78.51713337686715,
					108.4964215447043
				],
				[
					78.51713337686715,
					107.78261308569131
				],
				[
					78.51713337686715,
					107.42572247068907
				],
				[
					78.51713337686715,
					107.06883185568685
				],
				[
					78.51713337686715,
					106.35502339667383
				],
				[
					78.51713337686715,
					105.99813278167159
				],
				[
					78.51713337686715,
					105.28435155166713
				],
				[
					78.16024276186499,
					104.92746093666489
				],
				[
					78.16024276186499,
					104.21365247765189
				],
				[
					78.16024276186499,
					103.49987124764743
				],
				[
					78.16024276186499,
					102.78606278863441
				],
				[
					78.16024276186499,
					102.42917217363217
				],
				[
					78.16024276186499,
					101.71539094362771
				],
				[
					78.16024276186499,
					101.35850032862547
				],
				[
					78.16024276186499,
					101.35850032862547
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 164,
			"versionNonce": 1939626131,
			"isDeleted": false,
			"id": "3ot9sUrM9EpCeWCh_U1zb",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2356.7427839278907,
			"y": 6.967224673920043,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 17.13099458118404,
			"height": 9.636182750103018,
			"seed": 1572156689,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.3568906150021576,
					0.35689061500224284
				],
				[
					-1.0706718450064727,
					0.7137812300044573
				],
				[
					-1.0706718450064727,
					1.4275896890174806
				],
				[
					-1.427562460009085,
					1.784480304019695
				],
				[
					-2.4982615340240955,
					2.4982615340241807
				],
				[
					-3.568960608039106,
					3.2120699930371757
				],
				[
					-3.568960608039106,
					3.9258512230416613
				],
				[
					-4.639632453046033,
					4.996550297056899
				],
				[
					-5.710331527061044,
					5.710331527061356
				],
				[
					-6.067222142063656,
					6.424112757065814
				],
				[
					-6.424112757065814,
					6.781030601076594
				],
				[
					-7.1379212160786665,
					6.781030601076594
				],
				[
					-7.1379212160786665,
					7.49481183108108
				],
				[
					-7.494811831080824,
					7.49481183108108
				],
				[
					-7.494811831080824,
					7.851702446083294
				],
				[
					-8.208593061085594,
					7.851702446083294
				],
				[
					-7.851702446082982,
					7.851702446083294
				],
				[
					-7.494811831080824,
					7.851702446083294
				],
				[
					-6.424112757065814,
					7.851702446083294
				],
				[
					-5.353440912058886,
					6.781030601076594
				],
				[
					-3.568960608039106,
					5.710331527061356
				],
				[
					-2.4982615340240955,
					4.639632453046119
				],
				[
					-0.7137812300043151,
					3.5689606080394185
				],
				[
					0.7138084590128528,
					2.855152149026395
				],
				[
					0.7138084590128528,
					2.141370919021938
				],
				[
					1.7844803040197803,
					1.0706718450067
				],
				[
					2.8551793780347907,
					0.7137812300044573
				],
				[
					3.5689606080395606,
					0
				],
				[
					3.5689606080395606,
					-0.35689061500224284
				],
				[
					4.2827690670524134,
					-0.7138084590130234
				],
				[
					4.639659682054571,
					-0.7138084590130234
				],
				[
					4.639659682054571,
					-1.4275896890174806
				],
				[
					5.353440912059341,
					-1.4275896890174806
				],
				[
					5.353440912059341,
					-1.7844803040197235
				],
				[
					5.710358756070036,
					-1.7844803040197235
				],
				[
					5.710358756070036,
					-1.0706990740152378
				],
				[
					6.067249371072194,
					-1.0706990740152378
				],
				[
					6.067249371072194,
					-0.35689061500224284
				],
				[
					6.781030601076509,
					0.35689061500224284
				],
				[
					6.781030601076509,
					0.7137812300044573
				],
				[
					7.137921216079121,
					1.4275896890174806
				],
				[
					7.137921216079121,
					1.784480304019695
				],
				[
					7.851729675091974,
					2.4982615340241807
				],
				[
					7.851729675091974,
					2.855152149026395
				],
				[
					8.208620290094132,
					3.2120699930371757
				],
				[
					8.208620290094132,
					3.9258512230416613
				],
				[
					8.208620290094132,
					4.282741838043876
				],
				[
					8.922401520098447,
					4.282741838043876
				],
				[
					8.922401520098447,
					4.282741838043876
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 230,
			"versionNonce": 1700883997,
			"isDeleted": false,
			"id": "lYltBFx-Pa6xat4oZNI2t",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2254.313625368763,
			"y": -33.3620410885288,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 89.58090581598753,
			"height": 21.41376364823651,
			"seed": 155417073,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					1.0706990740150104,
					2.4982887630327184
				],
				[
					1.0706990740150104,
					2.855179378034933
				],
				[
					1.0706990740150104,
					3.5689606080394185
				],
				[
					1.427589689017168,
					4.2827690670524134
				],
				[
					1.427589689017168,
					5.3534409120591135
				],
				[
					1.427589689017168,
					6.424139986074351
				],
				[
					1.427589689017168,
					7.494811831081051
				],
				[
					1.427589689017168,
					7.851729675091832
				],
				[
					2.141370919021938,
					8.56551090509629
				],
				[
					2.141370919021938,
					9.636209979111555
				],
				[
					2.4982615340240955,
					9.99310059411377
				],
				[
					2.4982615340240955,
					10.349991209116013
				],
				[
					2.4982615340240955,
					11.06377243912047
				],
				[
					2.4982615340240955,
					11.42069028313125
				],
				[
					3.2120699930369483,
					12.134471513135708
				],
				[
					3.568960608039106,
					12.134471513135708
				],
				[
					4.282741838043876,
					12.134471513135708
				],
				[
					4.996550297056729,
					12.134471513135708
				],
				[
					7.851702446083436,
					11.777580898133493
				],
				[
					12.134471513135395,
					11.777580898133493
				],
				[
					15.703432121174956,
					11.06377243912047
				],
				[
					16.774103966181883,
					11.06377243912047
				],
				[
					21.77065426323861,
					11.06377243912047
				],
				[
					29.622383938330586,
					11.06377243912047
				],
				[
					35.33271546539163,
					11.06377243912047
				],
				[
					43.54130852647722,
					11.06377243912047
				],
				[
					45.6827066745077,
					11.06377243912047
				],
				[
					53.89129973559329,
					11.06377243912047
				],
				[
					60.315439721667644,
					11.06377243912047
				],
				[
					67.09647032274461,
					11.06377243912047
				],
				[
					70.30851308677302,
					11.06377243912047
				],
				[
					75.66195399883236,
					11.06377243912047
				],
				[
					78.87402399186931,
					11.06377243912047
				],
				[
					79.23091460687147,
					11.06377243912047
				],
				[
					80.30161368088693,
					11.06377243912047
				],
				[
					81.01539491089125,
					11.06377243912047
				],
				[
					81.37231275490194,
					11.06377243912047
				],
				[
					81.7292033699041,
					11.06377243912047
				],
				[
					82.44298459990887,
					11.06377243912047
				],
				[
					83.51368367392388,
					11.06377243912047
				],
				[
					84.5843555189308,
					11.06377243912047
				],
				[
					85.29816397794366,
					11.06377243912047
				],
				[
					86.36883582295059,
					11.06377243912047
				],
				[
					87.4395348969656,
					11.06377243912047
				],
				[
					88.15331612696991,
					11.06377243912047
				],
				[
					88.51023397098106,
					11.06377243912047
				],
				[
					88.86712458598322,
					11.06377243912047
				],
				[
					89.58090581598753,
					11.06377243912047
				],
				[
					89.58090581598753,
					10.706881824118256
				],
				[
					89.22401520098538,
					10.706881824118256
				],
				[
					88.86712458598322,
					10.706881824118256
				],
				[
					88.51023397098106,
					10.706881824118256
				],
				[
					87.79642551196775,
					10.706881824118256
				],
				[
					87.79642551196775,
					10.349991209116013
				],
				[
					87.4395348969656,
					10.349991209116013
				],
				[
					86.72575366696128,
					10.349991209116013
				],
				[
					86.36883582295059,
					10.349991209116013
				],
				[
					85.65505459294582,
					10.349991209116013
				],
				[
					85.65505459294582,
					10.706881824118256
				],
				[
					85.29816397794366,
					10.706881824118256
				],
				[
					85.29816397794366,
					11.42069028313125
				],
				[
					85.29816397794366,
					11.777580898133493
				],
				[
					84.9412733629415,
					12.49136212813795
				],
				[
					84.9412733629415,
					13.562061202153188
				],
				[
					84.9412733629415,
					13.918951817155431
				],
				[
					84.22746490392865,
					14.989650891170669
				],
				[
					84.22746490392865,
					15.346541506172912
				],
				[
					84.22746490392865,
					16.417213351179612
				],
				[
					83.87057428892604,
					17.131021810192607
				],
				[
					83.87057428892604,
					17.48791242519485
				],
				[
					83.87057428892604,
					17.844803040197093
				],
				[
					83.87057428892604,
					18.558611499210087
				],
				[
					83.87057428892604,
					18.91550211421233
				],
				[
					83.87057428892604,
					19.629283344216788
				],
				[
					83.15679305892172,
					19.272392729214573
				],
				[
					82.79987521491103,
					18.91550211421233
				],
				[
					82.08609398490671,
					18.91550211421233
				],
				[
					81.7292033699041,
					18.201693655199307
				],
				[
					80.65850429588909,
					17.844803040197093
				],
				[
					79.58783245088216,
					17.48791242519485
				],
				[
					79.23091460687147,
					16.774131195190392
				],
				[
					78.16024276186499,
					16.417213351179612
				],
				[
					77.80335214686238,
					16.417213351179612
				],
				[
					77.08954368784953,
					15.703432121175126
				],
				[
					76.73265307284737,
					15.703432121175126
				],
				[
					76.73265307284737,
					15.346541506172912
				],
				[
					76.01887184284305,
					15.346541506172912
				],
				[
					76.01887184284305,
					14.632733047159888
				],
				[
					76.01887184284305,
					14.989650891170669
				],
				[
					76.37576245784521,
					14.989650891170669
				],
				[
					76.73265307284737,
					15.346541506172912
				],
				[
					77.44643430285169,
					16.06032273617737
				],
				[
					77.80335214686238,
					17.131021810192607
				],
				[
					78.16024276186499,
					17.131021810192607
				],
				[
					78.87402399186931,
					17.844803040197093
				],
				[
					79.23091460687147,
					18.91550211421233
				],
				[
					79.94472306588477,
					19.629283344216788
				],
				[
					80.30161368088693,
					19.98617395921903
				],
				[
					81.01539491089125,
					19.98617395921903
				],
				[
					81.01539491089125,
					20.34309180322981
				],
				[
					81.37231275490194,
					21.056873033234268
				],
				[
					81.7292033699041,
					21.41376364823651
				],
				[
					82.44298459990887,
					21.41376364823651
				],
				[
					82.79987521491103,
					21.41376364823651
				],
				[
					83.51368367392388,
					21.41376364823651
				],
				[
					83.87057428892604,
					20.699982418232025
				],
				[
					84.5843555189308,
					20.699982418232025
				],
				[
					84.9412733629415,
					20.34309180322981
				],
				[
					85.29816397794366,
					19.98617395921903
				],
				[
					86.01194520794797,
					19.272392729214573
				],
				[
					86.36883582295059,
					18.91550211421233
				],
				[
					87.08264428196344,
					18.201693655199307
				],
				[
					87.4395348969656,
					18.201693655199307
				],
				[
					87.4395348969656,
					17.844803040197093
				],
				[
					88.15331612696991,
					17.844803040197093
				],
				[
					88.15331612696991,
					17.844803040197093
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 130,
			"versionNonce": 776588851,
			"isDeleted": false,
			"id": "5139CeVOGB8YSAvNC2d9U",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2187.577714724828,
			"y": -90.61079724143258,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 10.265249097825745,
			"height": 0.8212230605314801,
			"seed": 1904532927,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.8212387240587304,
					0
				],
				[
					1.2318424225609306,
					0
				],
				[
					2.053049819565331,
					0
				],
				[
					2.463653518067531,
					0
				],
				[
					3.2848922421258067,
					0.8212230605314801
				],
				[
					3.695495940628007,
					0.8212230605314801
				],
				[
					4.106099639130207,
					0.8212230605314801
				],
				[
					4.927338363188937,
					0.8212230605314801
				],
				[
					5.3379420616911375,
					0.8212230605314801
				],
				[
					6.159149458695538,
					0.8212230605314801
				],
				[
					6.569753157197738,
					0.8212230605314801
				],
				[
					6.980388182754268,
					0.8212230605314801
				],
				[
					7.8015955797586685,
					0.8212230605314801
				],
				[
					8.212199278260869,
					0.8212230605314801
				],
				[
					9.033438002319144,
					0.8212230605314801
				],
				[
					9.444041700821344,
					0.8212230605314801
				],
				[
					10.265249097825745,
					0.8212230605314801
				],
				[
					10.265249097825745,
					0.8212230605314801
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 247,
			"versionNonce": 245867133,
			"isDeleted": false,
			"id": "9UQtTKZZjUHhipfcxOYhh",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2189.6307645443935,
			"y": -86.91530130080451,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 172.045581144969,
			"height": 128.93151927057403,
			"seed": 1280277361,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.8212230605314801
				],
				[
					0,
					1.2318267590336802
				],
				[
					0,
					2.463653518067332
				],
				[
					0,
					3.6954959406280636
				],
				[
					0,
					4.927322699661744
				],
				[
					0,
					5.7485457601931955
				],
				[
					0,
					6.569753157197596
				],
				[
					0,
					7.801595579758327
				],
				[
					0,
					8.212199278260528
				],
				[
					0,
					8.622802976762728
				],
				[
					0,
					9.444026037294208
				],
				[
					0,
					9.85464539932346
				],
				[
					-0.41060369850220013,
					9.85464539932346
				],
				[
					-0.41060369850220013,
					10.67585279632786
				],
				[
					-0.8212073970044003,
					10.67585279632786
				],
				[
					-0.8212073970044003,
					11.08647215835714
				],
				[
					-1.6424461210631307,
					11.08647215835714
				],
				[
					-2.053049819565331,
					11.08647215835714
				],
				[
					-2.874257216569731,
					11.08647215835714
				],
				[
					-4.106099639130207,
					11.08647215835714
				],
				[
					-4.927307036134607,
					11.08647215835714
				],
				[
					-6.980356855699938,
					11.08647215835714
				],
				[
					-9.033406675264814,
					11.08647215835714
				],
				[
					-9.854645399323545,
					11.08647215835714
				],
				[
					-13.550110012897676,
					11.08647215835714
				],
				[
					-19.70925947159276,
					11.08647215835714
				],
				[
					-26.689647654347027,
					11.49707585685934
				],
				[
					-31.206350991979434,
					11.49707585685934
				],
				[
					-37.77610414917672,
					11.49707585685934
				],
				[
					-49.68379936806559,
					11.907695218888591
				],
				[
					-60.359667827920475,
					11.907695218888591
				],
				[
					-73.4991741423155,
					11.907695218888591
				],
				[
					-87.04931548226705,
					11.907695218888591
				],
				[
					-89.92357269883678,
					11.907695218888591
				],
				[
					-101.420664219223,
					11.907695218888591
				],
				[
					-108.40102107492294,
					12.728902615892991
				],
				[
					-110.04346719598561,
					13.550125676424472
				],
				[
					-110.86469025651695,
					13.960745038453723
				],
				[
					-112.09651701555094,
					14.781952435458123
				],
				[
					-112.50712071405314,
					15.603175495989603
				],
				[
					-113.32834377458448,
					16.424398556521055
				],
				[
					-113.32834377458448,
					16.835002255023255
				],
				[
					-113.32834377458448,
					18.066844677583987
				],
				[
					-113.32834377458448,
					18.477448376086187
				],
				[
					-113.73896313661362,
					18.477448376086187
				],
				[
					-114.14956683511582,
					18.477448376086187
				],
				[
					-114.97078989564761,
					18.477448376086187
				],
				[
					-115.38139359414981,
					18.477448376086187
				],
				[
					-116.20261665468115,
					18.477448376086187
				],
				[
					-116.61322035318335,
					18.477448376086187
				],
				[
					-117.43444341371469,
					18.477448376086187
				],
				[
					-117.84506277574383,
					18.477448376086187
				],
				[
					-117.84506277574383,
					19.29867143661764
				],
				[
					-117.84506277574383,
					19.70927513511984
				],
				[
					-118.25566647424603,
					20.94110189415352
				],
				[
					-119.07688953477782,
					22.58354801521645
				],
				[
					-121.1299393543427,
					26.689647654346714
				],
				[
					-122.77236981187889,
					30.385143594974778
				],
				[
					-123.18298917390803,
					31.61697035400843
				],
				[
					-125.6466426919751,
					37.365500450674574
				],
				[
					-127.69969251154043,
					43.52464990936997
				],
				[
					-128.11031187356957,
					45.1670960304329
				],
				[
					-130.5739653916371,
					50.9156417906261
				],
				[
					-133.44823827173377,
					61.180890888451756
				],
				[
					-135.91189178980085,
					68.1612634076786
				],
				[
					-136.32251115183044,
					69.3930745031852
				],
				[
					-140.01799142893128,
					80.0689586265672
				],
				[
					-141.66043754999419,
					87.04931548226699
				],
				[
					-142.48166061052552,
					89.10236530183212
				],
				[
					-143.30286800752992,
					96.08272215753192
				],
				[
					-143.7134873695593,
					103.06311034028585
				],
				[
					-143.7134873695593,
					105.11616015985095
				],
				[
					-143.7134873695593,
					111.27530961854637
				],
				[
					-143.7134873695593,
					116.61322035318324
				],
				[
					-143.7134873695593,
					117.43445907724174
				],
				[
					-143.7134873695593,
					120.3087162938113
				],
				[
					-143.7134873695593,
					121.9511624148742
				],
				[
					-143.30286800752992,
					123.18300483743496
				],
				[
					-143.30286800752992,
					123.59360853593716
				],
				[
					-143.30286800752992,
					124.41481593294156
				],
				[
					-142.48166061052552,
					124.82541963144376
				],
				[
					-142.48166061052552,
					125.64665835550227
				],
				[
					-141.24981818796482,
					125.64665835550227
				],
				[
					-139.60738773042908,
					125.64665835550227
				],
				[
					-135.0906687292695,
					125.64665835550227
				],
				[
					-128.93151927057397,
					125.64665835550227
				],
				[
					-115.38139359414981,
					125.64665835550227
				],
				[
					-109.22224413545428,
					126.46786575250667
				],
				[
					-93.61906863946479,
					126.46786575250667
				],
				[
					-89.51296900033458,
					126.46786575250667
				],
				[
					-71.03552062424842,
					127.28910447656523
				],
				[
					-56.664156223765076,
					127.28910447656523
				],
				[
					-32.84879711304211,
					128.11031187356963
				],
				[
					-28.742697473911903,
					128.11031187356963
				],
				[
					-13.550110012897676,
					128.93151927057403
				],
				[
					-2.874257216569731,
					128.93151927057403
				],
				[
					-0.8212073970044003,
					128.93151927057403
				],
				[
					4.516703337632407,
					128.93151927057403
				],
				[
					6.9803881827538135,
					128.93151927057403
				],
				[
					7.801595579758214,
					128.93151927057403
				],
				[
					8.212199278260414,
					128.93151927057403
				],
				[
					9.033438002319144,
					128.93151927057403
				],
				[
					9.444041700821344,
					128.93151927057403
				],
				[
					9.854645399323545,
					128.93151927057403
				],
				[
					10.675852796327945,
					128.93151927057403
				],
				[
					11.08648782188402,
					128.93151927057403
				],
				[
					11.90769521888842,
					128.93151927057403
				],
				[
					12.31829891739062,
					128.93151927057403
				],
				[
					13.139537641449351,
					128.93151927057403
				],
				[
					13.139537641449351,
					128.11031187356963
				],
				[
					13.550141339951551,
					128.11031187356963
				],
				[
					13.960745038453751,
					128.11031187356963
				],
				[
					14.781952435458152,
					128.11031187356963
				],
				[
					14.781952435458152,
					127.69970817506743
				],
				[
					15.192587461014227,
					126.87846945100887
				],
				[
					16.013794858018628,
					126.46786575250667
				],
				[
					16.013794858018628,
					126.05726205400447
				],
				[
					16.835002255023028,
					124.82541963144376
				],
				[
					17.65624097908176,
					122.7723698118786
				],
				[
					19.298687100144434,
					119.8981125953091
				],
				[
					20.530498195651035,
					117.84506277574394
				],
				[
					21.762340618211965,
					115.38140925767664
				],
				[
					23.40478673927464,
					112.50712071405297
				],
				[
					23.40478673927464,
					111.68591331704857
				],
				[
					24.63659783478124,
					110.04346719598561
				],
				[
					25.868440257342172,
					105.93736755685535
				],
				[
					26.279043955844372,
					103.88431773729025
				],
				[
					26.279043955844372,
					103.06311034028585
				],
				[
					27.100251352848773,
					101.01006052072069
				],
				[
					27.100251352848773,
					100.59945682221849
				],
				[
					27.100251352848773,
					99.36761439965778
				],
				[
					27.510886378405303,
					98.95701070115558
				],
				[
					27.510886378405303,
					98.13577197709708
				],
				[
					28.332093775409703,
					98.13577197709708
				],
				[
					28.332093775409703,
					97.72516827859488
				],
				[
					28.332093775409703,
					97.72516827859488
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 146,
			"versionNonce": 1257738195,
			"isDeleted": false,
			"id": "NWyeg--WJxOlanaJu7dAR",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2216.32041219874,
			"y": 7.525006062718603,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 11.497060193332345,
			"height": 4.106099639130264,
			"seed": 140968497,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-2.053049819565331,
					1.2318110955066004
				],
				[
					-2.874257216569731,
					1.6424147940088005
				],
				[
					-3.2848609150719312,
					2.0530498195651603
				],
				[
					-4.106099639130207,
					2.8742572165695606
				],
				[
					-4.106099639130207,
					3.2848609150717607
				],
				[
					-4.516703337632407,
					3.2848609150717607
				],
				[
					-4.516703337632407,
					4.106099639130264
				],
				[
					-4.927307036134607,
					4.106099639130264
				],
				[
					-4.927307036134607,
					3.695464613573961
				],
				[
					-4.516703337632407,
					3.2848609150717607
				],
				[
					-3.695495940628007,
					3.2848609150717607
				],
				[
					-3.2848609150719312,
					2.4636535180673604
				],
				[
					-2.463653518067531,
					1.6424147940088005
				],
				[
					-2.053049819565331,
					1.6424147940088005
				],
				[
					-2.053049819565331,
					0.8212073970044003
				],
				[
					-1.2318110955066004,
					0.8212073970044003
				],
				[
					-0.8212073970044003,
					0.8212073970044003
				],
				[
					-0.8212073970044003,
					0.41060369850220013
				],
				[
					-0.41060369850220013,
					0.41060369850220013
				],
				[
					0.41060369850220013,
					0.41060369850220013
				],
				[
					0.8212387240587304,
					0.41060369850220013
				],
				[
					1.6424461210631307,
					0.41060369850220013
				],
				[
					2.053049819565331,
					1.2318110955066004
				],
				[
					2.463653518067531,
					1.2318110955066004
				],
				[
					3.2848922421258067,
					1.6424147940088005
				],
				[
					3.695495940628007,
					1.6424147940088005
				],
				[
					3.695495940628007,
					2.0530498195651603
				],
				[
					4.516703337632407,
					2.0530498195651603
				],
				[
					4.516703337632407,
					2.8742572165695606
				],
				[
					4.927338363188937,
					2.8742572165695606
				],
				[
					5.748545760193338,
					3.2848609150717607
				],
				[
					6.159149458695538,
					3.2848609150717607
				],
				[
					6.159149458695538,
					4.106099639130264
				],
				[
					6.569753157197738,
					4.106099639130264
				],
				[
					6.569753157197738,
					4.106099639130264
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 206,
			"versionNonce": 770198237,
			"isDeleted": false,
			"id": "WKnv-FNL8AkRh2b2BEnZh",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2203.5915095828473,
			"y": -30.661733112014502,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 57.89599864632601,
			"height": 21.76234061821205,
			"seed": 950730641,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.8212073970044003,
					0
				],
				[
					1.2318424225604758,
					0.41060369850220013
				],
				[
					2.053049819564876,
					0.41060369850220013
				],
				[
					2.053049819564876,
					0.8212230605314801
				],
				[
					2.463653518067076,
					0.8212230605314801
				],
				[
					2.8742572165692764,
					0.8212230605314801
				],
				[
					3.695495940628007,
					1.6424304575358804
				],
				[
					4.927307036134607,
					2.053049819565132
				],
				[
					6.569753157197283,
					2.463653518067332
				],
				[
					9.033406675264814,
					3.284876578598812
				],
				[
					11.90769521888842,
					4.516703337632464
				],
				[
					14.371348736955952,
					5.748530096666144
				],
				[
					17.245605953525228,
					6.159149458695396
				],
				[
					20.530498195651035,
					7.390991881256127
				],
				[
					20.941101894153235,
					7.390991881256127
				],
				[
					24.22599413627904,
					8.622802976762728
				],
				[
					26.279043955844372,
					9.44404170082126
				],
				[
					28.742697473911903,
					9.85464539932346
				],
				[
					31.20635099197898,
					10.67585279632786
				],
				[
					32.84879711304211,
					11.08645649483006
				],
				[
					34.491243234104786,
					11.497091520386391
				],
				[
					35.312450631109186,
					12.318298917390791
				],
				[
					37.36550045067452,
					12.728902615892991
				],
				[
					40.650392692800324,
					13.550141339951523
				],
				[
					44.75649233193053,
					14.781952435458123
				],
				[
					48.45198827255854,
					16.013794858018855
				],
				[
					49.27319566956294,
					16.013794858018855
				],
				[
					50.50503809212387,
					16.424398556521055
				],
				[
					51.32624548912827,
					16.835002255023255
				],
				[
					52.14745288613267,
					16.835002255023255
				],
				[
					52.558087911688744,
					16.835002255023255
				],
				[
					53.379295308693145,
					17.656240979081787
				],
				[
					53.789899007195345,
					17.656240979081787
				],
				[
					53.789899007195345,
					18.066844677583987
				],
				[
					54.611137731254075,
					18.066844677583987
				],
				[
					55.021741429756275,
					18.066844677583987
				],
				[
					55.432345128258476,
					18.066844677583987
				],
				[
					56.253552525262876,
					18.066844677583987
				],
				[
					56.253552525262876,
					18.888052074588387
				],
				[
					56.664187550819406,
					18.888052074588387
				],
				[
					56.664187550819406,
					18.477448376086187
				],
				[
					56.664187550819406,
					18.066844677583987
				],
				[
					55.842948826760676,
					18.066844677583987
				],
				[
					55.842948826760676,
					17.245605953525455
				],
				[
					55.432345128258476,
					16.835002255023255
				],
				[
					55.021741429756275,
					16.835002255023255
				],
				[
					55.021741429756275,
					16.424398556521055
				],
				[
					54.200502705697545,
					15.603191159516655
				],
				[
					52.968691610190945,
					15.192556133960323
				],
				[
					52.968691610190945,
					14.371348736955923
				],
				[
					51.73684918763047,
					13.550141339951523
				],
				[
					51.32624548912827,
					13.550141339951523
				],
				[
					51.32624548912827,
					12.728902615892991
				],
				[
					50.91564179062607,
					12.728902615892991
				],
				[
					50.09440306656734,
					12.318298917390791
				],
				[
					49.68379936806514,
					11.497091520386391
				],
				[
					50.50503809212387,
					11.907695218888591
				],
				[
					50.91564179062607,
					12.318298917390791
				],
				[
					51.32624548912827,
					12.318298917390791
				],
				[
					52.14745288613267,
					13.139506314395192
				],
				[
					52.558087911688744,
					13.550141339951523
				],
				[
					53.379295308693145,
					13.960745038453723
				],
				[
					53.789899007195345,
					13.960745038453723
				],
				[
					53.789899007195345,
					14.781952435458123
				],
				[
					54.611137731254075,
					15.192556133960323
				],
				[
					55.021741429756275,
					16.013794858018855
				],
				[
					55.432345128258476,
					16.424398556521055
				],
				[
					56.253552525262876,
					16.424398556521055
				],
				[
					56.253552525262876,
					16.835002255023255
				],
				[
					56.664187550819406,
					17.656240979081787
				],
				[
					57.485394947823806,
					17.656240979081787
				],
				[
					57.485394947823806,
					18.066844677583987
				],
				[
					57.89599864632601,
					18.888052074588387
				],
				[
					57.89599864632601,
					19.298655773090587
				],
				[
					57.89599864632601,
					20.11989449714912
				],
				[
					57.89599864632601,
					20.53049819565132
				],
				[
					57.89599864632601,
					20.94110189415352
				],
				[
					57.89599864632601,
					21.76234061821205
				],
				[
					57.074791249321606,
					21.76234061821205
				],
				[
					55.842948826760676,
					21.76234061821205
				],
				[
					55.432345128258476,
					21.76234061821205
				],
				[
					55.021741429756275,
					21.35170559265572
				],
				[
					54.200502705697545,
					21.35170559265572
				],
				[
					52.968691610190945,
					21.35170559265572
				],
				[
					52.558087911688744,
					20.94110189415352
				],
				[
					51.32624548912827,
					20.94110189415352
				],
				[
					50.09440306656734,
					20.94110189415352
				],
				[
					49.68379936806514,
					20.94110189415352
				],
				[
					48.86259197106074,
					20.94110189415352
				],
				[
					47.63074954850026,
					20.94110189415352
				],
				[
					46.80954215149586,
					20.94110189415352
				],
				[
					45.98830342743713,
					20.94110189415352
				],
				[
					45.98830342743713,
					21.76234061821205
				],
				[
					45.57769972893493,
					21.76234061821205
				],
				[
					45.57769972893493,
					21.76234061821205
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 133,
			"versionNonce": 1002184051,
			"isDeleted": false,
			"id": "B5g5t86d",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2102.423090397567,
			"y": 62.590476832863146,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 259.21978759765625,
			"height": 25,
			"seed": 1971759699,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158218,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Time Complexity : O(nLogn)",
			"rawText": "Time Complexity : O(nLogn)",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Time Complexity : O(nLogn)",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 180,
			"versionNonce": 62187325,
			"isDeleted": false,
			"id": "IV7SiSjZ",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2111.3090221825846,
			"y": 104.46335942161761,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 229.07980346679688,
			"height": 25,
			"seed": 655948893,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Space Complexity : O(n)",
			"rawText": "Space Complexity : O(n)",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Space Complexity : O(n)",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1617,
			"versionNonce": 1809708819,
			"isDeleted": false,
			"id": "4xNJVlgW5R82yvcFkILUx",
			"fillStyle": "solid",
			"strokeWidth": 4,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1992.0817022977767,
			"y": 219.94601170633842,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 810.7795986610721,
			"height": 542.2523373967291,
			"seed": 1552437779,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 1517,
			"versionNonce": 1114568605,
			"isDeleted": false,
			"id": "QyoEyPdR",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2318.9040492767494,
			"y": 248.19060354849444,
			"strokeColor": "#e03131",
			"backgroundColor": "transparent",
			"width": 143.86392211914062,
			"height": 35,
			"seed": 2042615517,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Quick Sort",
			"rawText": "Quick Sort",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Quick Sort",
			"lineHeight": 1.25
		},
		{
			"type": "ellipse",
			"version": 894,
			"versionNonce": 433298611,
			"isDeleted": false,
			"id": "w3cfXXgW0r51ltg39xijt",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2698.3458565314722,
			"y": 243.71287987959153,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 80.9803541126721,
			"height": 85.47926267448713,
			"seed": 1472999517,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "hVb1ogJm"
				}
			],
			"updated": 1715421158219,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 825,
			"versionNonce": 1414003709,
			"isDeleted": false,
			"id": "hVb1ogJm",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2727.9951557353565,
			"y": 268.7310280728571,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 21.419998168945312,
			"height": 35,
			"seed": 1660951741,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "8",
			"rawText": "8",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "w3cfXXgW0r51ltg39xijt",
			"originalText": "8",
			"lineHeight": 1.25
		},
		{
			"type": "rectangle",
			"version": 1004,
			"versionNonce": 1900252755,
			"isDeleted": false,
			"id": "_uRL-j9RZDDwKtRIDRWgw",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2388.058739679032,
			"y": 385.7213080815998,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 402.4000244140622,
			"height": 312.59322735608,
			"seed": 1095643923,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 402,
			"versionNonce": 1631679581,
			"isDeleted": false,
			"id": "ZvROuNCQ",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2430.844304881805,
			"y": 406.2107969153133,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 309.4198913574219,
			"height": 25,
			"seed": 1527070931,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[ 10, 80, 30, 90, 40, 50, 70 ]",
			"rawText": "[ 10, 80, 30, 90, 40, 50, 70 ]",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[ 10, 80, 30, 90, 40, 50, 70 ]",
			"lineHeight": 1.25
		},
		{
			"type": "ellipse",
			"version": 186,
			"versionNonce": 1694780403,
			"isDeleted": false,
			"id": "nRBdqKjXEyOE3W2mzOD-r",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2689.1942633028584,
			"y": 395.3427700253074,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 38.53057933929949,
			"height": 40.67110356952412,
			"seed": 2113966461,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 276,
			"versionNonce": 355262653,
			"isDeleted": false,
			"id": "C1r57hJF",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2400.2153537610675,
			"y": 465.98200216708193,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 184.4799346923828,
			"height": 25,
			"seed": 1215770579,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[ 10, 30, 40, 50 ]",
			"rawText": "[ 10, 30, 40, 50 ]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[ 10, 30, 40, 50 ]",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 303,
			"versionNonce": 1226593683,
			"isDeleted": false,
			"id": "fTJqV4MM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2635.6794427543605,
			"y": 468.83612520383036,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 109.9599609375,
			"height": 25,
			"seed": 569546141,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[ 90, 80 ]",
			"rawText": "[ 90, 80 ]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[ 90, 80 ]",
			"lineHeight": 1.25
		},
		{
			"type": "ellipse",
			"version": 221,
			"versionNonce": 632013085,
			"isDeleted": false,
			"id": "_skevP1nIX2_fCKLxwZZ9",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2532.2179862225203,
			"y": 457.41966027577126,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 39.957668076608115,
			"height": 39.24406927008453,
			"seed": 1475657619,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 265,
			"versionNonce": 750922547,
			"isDeleted": false,
			"id": "HX4IBdd8fFp1fctUMbvXH",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2692.7619034893273,
			"y": 460.27383775038896,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 39.24404205114979,
			"height": 38.53052490143011,
			"seed": 1763753341,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 160,
			"versionNonce": 405771645,
			"isDeleted": false,
			"id": "0N8Un32r",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2403.7829939475355,
			"y": 535.1942816662206,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 143.21995544433594,
			"height": 25,
			"seed": 1394688093,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[ 10, 30, 40 ]",
			"rawText": "[ 10, 30, 40 ]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[ 10, 30, 40 ]",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 146,
			"versionNonce": 1952206035,
			"isDeleted": false,
			"id": "wNV0U12M",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2572.88906257311,
			"y": 534.4807645165008,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 29.819992065429688,
			"height": 25,
			"seed": 1621263997,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[ ]",
			"rawText": "[ ]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[ ]",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 200,
			"versionNonce": 1207557597,
			"isDeleted": false,
			"id": "AtlrsqaH",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2396.9256638346174,
			"y": 592.0848724054529,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 101.51997375488281,
			"height": 25,
			"seed": 2126404051,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[ 10, 30 ]",
			"rawText": "[ 10, 30 ]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[ 10, 30 ]",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 202,
			"versionNonce": 864107123,
			"isDeleted": false,
			"id": "0JsKTmEn",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2543.708560232392,
			"y": 593.3335138079951,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 29.819992065429688,
			"height": 25,
			"seed": 1017460179,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[ ]",
			"rawText": "[ ]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[ ]",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 217,
			"versionNonce": 740039229,
			"isDeleted": false,
			"id": "VR3wLF4i",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2400.82941823149,
			"y": 646.6697781459898,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 58.99998474121094,
			"height": 25,
			"seed": 539870525,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[ 10 ]",
			"rawText": "[ 10 ]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[ 10 ]",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 247,
			"versionNonce": 1190622227,
			"isDeleted": false,
			"id": "FQMQdXOY",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2503.7510010315223,
			"y": 646.134599455298,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 29.819992065429688,
			"height": 25,
			"seed": 2088913949,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[ ]",
			"rawText": "[ ]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[ ]",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 380,
			"versionNonce": 1568131741,
			"isDeleted": false,
			"id": "uZvmjxiM",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2712.5239196016423,
			"y": 534.1106649374758,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 55.759979248046875,
			"height": 25,
			"seed": 620285747,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[ 90]",
			"rawText": "[ 90]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[ 90]",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 200,
			"versionNonce": 783645107,
			"isDeleted": false,
			"id": "yA6rhPSq",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2643.959325685164,
			"y": 535.002629421962,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"width": 29.819992065429688,
			"height": 25,
			"seed": 636141661,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "[ ]",
			"rawText": "[ ]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[ ]",
			"lineHeight": 1.25
		},
		{
			"type": "ellipse",
			"version": 290,
			"versionNonce": 1555984125,
			"isDeleted": false,
			"id": "VXMRwgAazZkwLidaOg5As",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2495.47125419539,
			"y": 523.207940131945,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 39.957668076608115,
			"height": 39.24406927008453,
			"seed": 1910791763,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 298,
			"versionNonce": 669109075,
			"isDeleted": false,
			"id": "W_xmeQUWDZBzZuBRou6P_",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2446.4162560693217,
			"y": 581.5735360429705,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 39.957668076608115,
			"height": 39.24406927008453,
			"seed": 182444605,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false
		},
		{
			"type": "freedraw",
			"version": 150,
			"versionNonce": 339582365,
			"isDeleted": false,
			"id": "WQ3nmIDPj2m6BL2xXkZC3",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2556.0195318515043,
			"y": 434.6419064907195,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 53.56211972408664,
			"height": 31.866070246088157,
			"seed": 1249262717,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.22601425548691623,
					0
				],
				[
					-0.4520112685067943,
					0.22600563425311293
				],
				[
					-1.1300023075659738,
					0.6779996602925848
				],
				[
					-1.8080105890917366,
					1.130002307565519
				],
				[
					-2.7120158836378323,
					1.8080019678581607
				],
				[
					-3.6160211781834732,
					2.0340076021113305
				],
				[
					-4.520009230262531,
					2.486010249384208
				],
				[
					-5.65001153782805,
					2.9380042754236797
				],
				[
					-7.68401913993921,
					3.842009569969491
				],
				[
					-9.944023755070248,
					4.520009230262133
				],
				[
					-12.204028370201286,
					4.97201187753501
				],
				[
					-14.464032985332324,
					5.650011537827652
				],
				[
					-17.1760488689697,
					6.102014185100529
				],
				[
					-19.888047510140495,
					6.780013845393171
				],
				[
					-22.600046151310835,
					7.232016492666105
				],
				[
					-25.312062034948212,
					7.684019139938982
				],
				[
					-28.024060676119007,
					7.910016152958747
				],
				[
					-30.284065291250045,
					8.362018800231624
				],
				[
					-32.09207588034178,
					9.040018460524266
				],
				[
					-33.6740722139466,
					9.4920211077972
				],
				[
					-34.80407452151212,
					9.718018120816907
				],
				[
					-35.25608579001846,
					9.944023755070077
				],
				[
					-35.70807981605776,
					9.944023755070077
				],
				[
					-36.38608809758398,
					10.396026402342954
				],
				[
					-36.61208511060386,
					10.396026402342954
				],
				[
					-37.06407913664316,
					10.396026402342954
				],
				[
					-37.06407913664316,
					10.622023415362719
				],
				[
					-37.29007614966304,
					10.622023415362719
				],
				[
					-37.5160904051495,
					10.622023415362719
				],
				[
					-37.9680844311888,
					10.622023415362719
				],
				[
					-38.19408144420868,
					10.622023415362719
				],
				[
					-38.19408144420868,
					11.074026062635596
				],
				[
					-38.19408144420868,
					11.752025722928238
				],
				[
					-38.19408144420868,
					12.65603101747405
				],
				[
					-38.19408144420868,
					13.560027690786399
				],
				[
					-38.19408144420868,
					14.916035632605144
				],
				[
					-38.64609271271502,
					15.820032305917493
				],
				[
					-38.872089725734895,
					16.724037600463305
				],
				[
					-38.872089725734895,
					18.08003692104853
				],
				[
					-39.09808673875477,
					19.436044862867277
				],
				[
					-39.550080764794075,
					20.340041536179626
				],
				[
					-39.550080764794075,
					21.470043843745202
				],
				[
					-39.776095020280536,
					22.374049138290957
				],
				[
					-40.22808904632029,
					23.278045811603363
				],
				[
					-40.454086059339716,
					23.95605409312941
				],
				[
					-40.454086059339716,
					24.63405375342205
				],
				[
					-40.906097327846055,
					25.312053413714693
				],
				[
					-40.906097327846055,
					25.76405606098757
				],
				[
					-41.13209434086593,
					26.216058708260505
				],
				[
					-41.13209434086593,
					26.442055721280212
				],
				[
					-41.35809135388581,
					26.894058368553146
				],
				[
					-41.35809135388581,
					27.120055381572854
				],
				[
					-41.35809135388581,
					27.57205802884573
				],
				[
					-41.35809135388581,
					27.346061015826024
				],
				[
					-41.81008537992511,
					27.346061015826024
				],
				[
					-42.036099635411574,
					27.346061015826024
				],
				[
					-42.48809366145133,
					27.120055381572854
				],
				[
					-43.16610194297709,
					26.668052734299977
				],
				[
					-43.61809596901685,
					26.442055721280212
				],
				[
					-45.65210357112801,
					25.538050426734458
				],
				[
					-46.55610886567365,
					24.86005076644176
				],
				[
					-47.46009691775271,
					24.408048119168882
				],
				[
					-49.720101532883746,
					23.504051445856533
				],
				[
					-50.62410682742984,
					22.82605178556389
				],
				[
					-51.980106148014784,
					22.374049138290957
				],
				[
					-52.658114429541,
					22.148043504037787
				],
				[
					-52.658114429541,
					21.92204649101808
				],
				[
					-52.88411144256088,
					21.92204649101808
				],
				[
					-53.33612271106722,
					21.92204649101808
				],
				[
					-53.33612271106722,
					21.470043843745202
				],
				[
					-53.56211972408664,
					21.470043843745202
				],
				[
					-53.56211972408664,
					21.92204649101808
				],
				[
					-53.56211972408664,
					22.60004615131072
				],
				[
					-53.1101084555803,
					23.95605409312941
				],
				[
					-52.43211741652112,
					24.86005076644176
				],
				[
					-52.2061204035017,
					25.76405606098757
				],
				[
					-51.52811212197548,
					26.668052734299977
				],
				[
					-51.302115108955604,
					27.798055041865496
				],
				[
					-50.62410682742984,
					28.702060336411307
				],
				[
					-50.172112801390085,
					29.38005999670395
				],
				[
					-49.720101532883746,
					30.284065291249703
				],
				[
					-49.720101532883746,
					30.510062304269468
				],
				[
					-49.268107506844444,
					30.962064951542402
				],
				[
					-49.042110493824566,
					31.18806196456211
				],
				[
					-49.042110493824566,
					31.640064611834987
				],
				[
					-48.59009922531823,
					31.640064611834987
				],
				[
					-48.3641022122988,
					31.640064611834987
				],
				[
					-48.3641022122988,
					31.866070246088157
				],
				[
					-48.138105199278925,
					31.866070246088157
				],
				[
					-47.686111173239624,
					31.866070246088157
				],
				[
					-47.46009691775271,
					31.866070246088157
				],
				[
					-47.008102891713406,
					31.866070246088157
				],
				[
					-46.33009461018719,
					31.866070246088157
				],
				[
					-45.87810058414789,
					31.18806196456211
				],
				[
					-45.20009230262167,
					30.510062304269468
				],
				[
					-44.52210126356249,
					30.284065291249703
				],
				[
					-44.07008999505615,
					29.832062643976826
				],
				[
					-43.61809596901685,
					29.154062983684184
				],
				[
					-42.94008768749063,
					28.928057349431015
				],
				[
					-42.26209664843145,
					28.25005768913843
				],
				[
					-42.036099635411574,
					28.024060676118665
				],
				[
					-41.35809135388581,
					27.346061015826024
				],
				[
					-40.680083072359594,
					26.894058368553146
				],
				[
					-40.22808904632029,
					26.668052734299977
				],
				[
					-40.002092033300414,
					26.442055721280212
				],
				[
					-39.776095020280536,
					25.990053074007335
				],
				[
					-39.776095020280536,
					25.76405606098757
				],
				[
					-39.3240837517742,
					25.76405606098757
				],
				[
					-39.09808673875477,
					25.312053413714693
				],
				[
					-38.64609271271502,
					25.312053413714693
				],
				[
					-38.872089725734895,
					25.312053413714693
				],
				[
					-38.872089725734895,
					25.538050426734458
				],
				[
					-38.872089725734895,
					25.538050426734458
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 169,
			"versionNonce": 237655731,
			"isDeleted": false,
			"id": "lKxCfWuUPMqJaItoNaV8e",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2612.0676359612744,
			"y": 432.15590486256866,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 48.59009922531823,
			"height": 32.09206725910798,
			"seed": 2127190941,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					2.034024844578198,
					0.9039966733124061
				],
				[
					2.711998641170794,
					1.1300023075655758
				],
				[
					3.6160211781834732,
					1.3559993205852834
				],
				[
					4.520009230262531,
					2.033998980877925
				],
				[
					5.876025793314511,
					2.033998980877925
				],
				[
					6.780013845393569,
					2.4860016281508592
				],
				[
					8.58802443448485,
					2.712007262403972
				],
				[
					9.944040997537286,
					2.712007262403972
				],
				[
					11.526037331142106,
					3.164001288443444
				],
				[
					12.882019409260465,
					3.164001288443444
				],
				[
					14.690029998352202,
					3.164001288443444
				],
				[
					16.046046561404182,
					3.164001288443444
				],
				[
					17.1760488689697,
					3.164001288443444
				],
				[
					18.53203094708806,
					3.164001288443444
				],
				[
					19.888047510140495,
					2.9380042754237365
				],
				[
					20.792035562219553,
					2.9380042754237365
				],
				[
					21.922037869785072,
					2.712007262403972
				],
				[
					22.374066380757995,
					2.4860016281508592
				],
				[
					23.05204017735059,
					2.033998980877925
				],
				[
					23.730048458876354,
					1.8080019678582175
				],
				[
					24.18204248491611,
					1.8080019678582175
				],
				[
					24.634070995889033,
					1.3559993205852834
				],
				[
					25.31204479248163,
					1.3559993205852834
				],
				[
					25.990053074007392,
					1.1300023075655758
				],
				[
					26.216067329494308,
					1.1300023075655758
				],
				[
					26.89407561102007,
					1.1300023075655758
				],
				[
					27.572049407612667,
					1.1300023075655758
				],
				[
					28.250057689138885,
					1.1300023075655758
				],
				[
					28.928065970664647,
					1.1300023075655758
				],
				[
					29.15408022615111,
					1.1300023075655758
				],
				[
					29.606074252190865,
					1.1300023075655758
				],
				[
					29.832054022743705,
					1.1300023075655758
				],
				[
					30.284082533717083,
					1.1300023075655758
				],
				[
					30.510062304269923,
					1.1300023075655758
				],
				[
					30.510062304269923,
					1.5820049548384532
				],
				[
					30.736076559756384,
					1.5820049548384532
				],
				[
					31.188070585795685,
					1.8080019678582175
				],
				[
					31.4140848412826,
					1.8080019678582175
				],
				[
					31.866078867321903,
					2.260004615131095
				],
				[
					32.09205863787474,
					2.260004615131095
				],
				[
					32.318072893361204,
					2.4860016281508592
				],
				[
					32.77006691940096,
					2.712007262403972
				],
				[
					32.99608117488742,
					3.164001288443444
				],
				[
					33.44807520092672,
					3.390006922696614
				],
				[
					33.44807520092672,
					3.842009569969548
				],
				[
					33.67408945641364,
					4.746006243281897
				],
				[
					34.35206325300578,
					5.424005903574539
				],
				[
					34.57807750849224,
					6.32801119812035
				],
				[
					35.030071534532,
					7.232016492666162
				],
				[
					35.25608579001846,
					8.588015813251388
				],
				[
					35.93409407154468,
					9.4920211077972
				],
				[
					36.38608809758398,
					10.622023415362776
				],
				[
					36.61206786813682,
					11.526020088675125
				],
				[
					37.0640963791102,
					12.882028030493814
				],
				[
					37.29007614966304,
					13.78602470380622
				],
				[
					37.5160904051495,
					14.464024364098861
				],
				[
					37.9680844311888,
					15.368029658644616
				],
				[
					38.194098686675716,
					16.498031966210192
				],
				[
					38.64609271271502,
					16.95003461348307
				],
				[
					38.87207248326786,
					18.08003692104859
				],
				[
					39.550080764794075,
					18.984033594360994
				],
				[
					39.776095020280536,
					20.340041536179683
				],
				[
					40.22808904631984,
					21.018041196472325
				],
				[
					40.906097327846055,
					21.922046491018136
				],
				[
					41.132077098398895,
					22.600046151310778
				],
				[
					41.35809135388581,
					23.278045811603363
				],
				[
					41.35809135388581,
					23.504042824623127
				],
				[
					41.81008537992511,
					23.730048458876297
				],
				[
					41.81008537992511,
					24.18205110614923
				],
				[
					41.81008537992511,
					24.40804811916894
				],
				[
					42.036099635411574,
					24.40804811916894
				],
				[
					42.036099635411574,
					24.860050766441816
				],
				[
					42.036099635411574,
					25.08604777946158
				],
				[
					41.58410560937227,
					25.08604777946158
				],
				[
					41.58410560937227,
					24.634045132188646
				],
				[
					41.35809135388581,
					24.634045132188646
				],
				[
					41.132077098398895,
					24.40804811916894
				],
				[
					40.680083072359594,
					24.40804811916894
				],
				[
					40.454103301806754,
					24.40804811916894
				],
				[
					40.002074790833376,
					23.95604547189606
				],
				[
					39.324100994241235,
					23.95604547189606
				],
				[
					38.420078457228556,
					23.504042824623127
				],
				[
					38.194098686675716,
					23.504042824623127
				],
				[
					37.5160904051495,
					23.052048798583655
				],
				[
					36.83808212362328,
					23.052048798583655
				],
				[
					36.61206786813682,
					22.826043164330486
				],
				[
					35.93409407154468,
					22.374040517057608
				],
				[
					35.25608579001846,
					22.148043504037844
				],
				[
					34.57807750849224,
					21.696040856764967
				],
				[
					33.90006922696648,
					21.470043843745202
				],
				[
					33.67408945641364,
					21.24403820949209
				],
				[
					33.22206094544026,
					21.24403820949209
				],
				[
					33.22206094544026,
					20.79204418345256
				],
				[
					32.99608117488742,
					20.79204418345256
				],
				[
					33.44807520092672,
					21.24403820949209
				],
				[
					33.67408945641364,
					21.922046491018136
				],
				[
					34.35206325300578,
					22.826043164330486
				],
				[
					35.25608579001846,
					23.730048458876297
				],
				[
					36.61206786813682,
					25.764047439754222
				],
				[
					37.9680844311888,
					27.12005538157291
				],
				[
					38.87207248326786,
					28.476054702158194
				],
				[
					40.002074790833376,
					29.380059996704006
				],
				[
					40.454103301806754,
					30.05805965699659
				],
				[
					40.906097327846055,
					30.73605931728929
				],
				[
					41.58410560937227,
					30.962064951542402
				],
				[
					41.81008537992511,
					31.414058977581874
				],
				[
					41.81008537992511,
					31.640064611835044
				],
				[
					42.262079405964414,
					32.09206725910798
				],
				[
					42.48809366145133,
					32.09206725910798
				],
				[
					42.71410791693779,
					32.09206725910798
				],
				[
					43.16610194297709,
					32.09206725910798
				],
				[
					43.39208171352993,
					32.09206725910798
				],
				[
					43.84411022450331,
					32.09206725910798
				],
				[
					44.07008999505615,
					31.866061624854808
				],
				[
					44.52208402109545,
					31.640064611835044
				],
				[
					44.74809827658237,
					31.188061964562166
				],
				[
					44.97411253206883,
					30.510062304269525
				],
				[
					45.42610655810813,
					30.284056670016355
				],
				[
					46.10411483963435,
					29.380059996704006
				],
				[
					46.33009461018719,
					28.476054702158194
				],
				[
					47.008102891713406,
					27.12005538157291
				],
				[
					47.008102891713406,
					26.668052734300034
				],
				[
					47.23411714719987,
					26.2160500870271
				],
				[
					47.68611117323917,
					25.538050426734458
				],
				[
					47.68611117323917,
					24.860050766441816
				],
				[
					47.912090943792464,
					24.18205110614923
				],
				[
					47.912090943792464,
					23.95604547189606
				],
				[
					48.36411945476539,
					23.504042824623127
				],
				[
					48.36411945476539,
					23.278045811603363
				],
				[
					48.59009922531823,
					23.278045811603363
				],
				[
					48.59009922531823,
					22.826043164330486
				],
				[
					48.59009922531823,
					22.826043164330486
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 123,
			"versionNonce": 22143485,
			"isDeleted": false,
			"id": "Ps2AtJeX-KkHs7fwk0QFY",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2489.0647023116207,
			"y": 497.00528009623326,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 23.452913930431805,
			"height": 33.56196738442986,
			"seed": 1809083603,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.4043701592349862
				],
				[
					0,
					0.8087248933255751
				],
				[
					0,
					1.2130950525605613
				],
				[
					0,
					2.021804520741796
				],
				[
					-0.40435473409070255,
					3.234899573302414
				],
				[
					-0.40435473409070255,
					3.639254307393003
				],
				[
					-1.213064202271653,
					5.25670409404421
				],
				[
					-2.426159254832328,
					6.469783721460431
				],
				[
					-2.8305139889230304,
					8.087218082967297
				],
				[
					-3.234868723013733,
					9.300313135527858
				],
				[
					-4.447963775573953,
					10.513392762944136
				],
				[
					-5.256673243755358,
					12.130827124451002
				],
				[
					-6.469768296316033,
					13.343922177011564
				],
				[
					-6.874123030406736,
					14.152631645192798
				],
				[
					-7.278477764497438,
					15.365726697753416
				],
				[
					-7.278477764497438,
					15.770081431844005
				],
				[
					-8.08721808296741,
					16.174436165934594
				],
				[
					-8.491572817057659,
					16.983161059260283
				],
				[
					-9.300282285239064,
					17.38753121849527
				],
				[
					-9.300282285239064,
					18.196240686676447
				],
				[
					-9.704667869618333,
					18.196240686676447
				],
				[
					-9.704667869618333,
					18.600610845911433
				],
				[
					-10.109022603709036,
					18.600610845911433
				],
				[
					-10.109022603709036,
					19.004965580002136
				],
				[
					-10.109022603709036,
					19.81369047332771
				],
				[
					-10.917732071890441,
					19.81369047332771
				],
				[
					-10.917732071890441,
					20.2180452074183
				],
				[
					-11.322086805980689,
					20.2180452074183
				],
				[
					-11.322086805980689,
					21.026770100743875
				],
				[
					-12.130827124450661,
					21.43114025997886
				],
				[
					-12.130827124450661,
					22.239849728160152
				],
				[
					-12.130827124450661,
					22.64421988739514
				],
				[
					-12.535181858541364,
					23.048574621485727
				],
				[
					-12.535181858541364,
					23.857299514811302
				],
				[
					-13.343891326722769,
					23.857299514811302
				],
				[
					-13.343891326722769,
					24.261654248902005
				],
				[
					-13.343891326722769,
					25.07037914222758
				],
				[
					-13.748276911102039,
					25.07037914222758
				],
				[
					-13.748276911102039,
					25.474749301462566
				],
				[
					-14.152631645192741,
					25.474749301462566
				],
				[
					-14.961341113374147,
					24.261654248902005
				],
				[
					-15.365695847464394,
					23.452944780720713
				],
				[
					-16.57879090002507,
					22.64421988739514
				],
				[
					-17.387500368206474,
					20.622415366653286
				],
				[
					-17.791885952585744,
					19.409335739237008
				],
				[
					-19.004950154857397,
					17.791885952585858
				],
				[
					-20.218045207418072,
					16.174436165934594
				],
				[
					-21.026754675599477,
					14.557001804427784
				],
				[
					-21.83549499406945,
					12.535197283685989
				],
				[
					-22.239849728160152,
					12.130827124451002
				],
				[
					-22.239849728160152,
					11.726472390360357
				],
				[
					-23.048559196341103,
					10.917747497034725
				],
				[
					-23.452913930431805,
					10.917747497034725
				],
				[
					-22.644204462250855,
					11.322117656269711
				],
				[
					-22.239849728160152,
					12.130827124451002
				],
				[
					-21.43110940969018,
					14.152631645192798
				],
				[
					-21.026754675599477,
					15.365726697753416
				],
				[
					-20.622399941508775,
					16.983161059260283
				],
				[
					-19.81369047332737,
					18.600610845911433
				],
				[
					-19.81369047332737,
					20.2180452074183
				],
				[
					-19.4093048889481,
					22.239849728160152
				],
				[
					-18.60059542076715,
					23.048574621485727
				],
				[
					-18.196240686676447,
					25.07037914222758
				],
				[
					-16.983145634115772,
					26.687828928878844
				],
				[
					-16.57879090002507,
					28.305263290385597
				],
				[
					-15.770081431844119,
					29.518358342946158
				],
				[
					-15.365695847464394,
					30.731437970362435
				],
				[
					-14.152631645192741,
					31.135792704453024
				],
				[
					-14.152631645192741,
					31.944517597778713
				],
				[
					-13.748276911102039,
					32.3488723318693
				],
				[
					-12.939536592632066,
					33.15759722519488
				],
				[
					-12.535181858541364,
					33.56196738442986
				],
				[
					-11.726472390360414,
					33.56196738442986
				],
				[
					-11.322086805980689,
					32.75324249110429
				],
				[
					-10.513377337799739,
					32.3488723318693
				],
				[
					-10.109022603709036,
					30.32706781112745
				],
				[
					-8.895927551148361,
					29.518358342946158
				],
				[
					-8.491572817057659,
					28.305263290385597
				],
				[
					-7.682863348876708,
					27.092183662969433
				],
				[
					-7.278477764497438,
					26.687828928878844
				],
				[
					-7.278477764497438,
					25.879104035553155
				],
				[
					-6.874123030406736,
					25.474749301462566
				],
				[
					-6.874123030406736,
					24.66602440813699
				],
				[
					-6.065413562225331,
					24.66602440813699
				],
				[
					-6.065413562225331,
					24.261654248902005
				],
				[
					-6.065413562225331,
					24.261654248902005
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 157,
			"versionNonce": 712279539,
			"isDeleted": false,
			"id": "jXHt70uPnUf8pp6aV7uTP",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2524.2440886324134,
			"y": 494.5791208414008,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 67.12393476885973,
			"height": 31.540147438543613,
			"seed": 1008628275,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.8087711687585397,
					0.8087248933255751
				],
				[
					1.2130950525602202,
					0.8087248933255751
				],
				[
					2.426190105120895,
					1.6174497866511501
				],
				[
					3.63928515768157,
					2.8305294140674278
				],
				[
					4.852380210242245,
					3.639254307393003
				],
				[
					6.4697991466046005,
					4.447963775574237
				],
				[
					8.087218082966956,
					5.6610588281348555
				],
				[
					9.7046987199069,
					6.874138455551019
				],
				[
					12.130827124451116,
					8.087218082967297
				],
				[
					15.770112282132686,
					10.10902260370915
				],
				[
					18.600626271055717,
					11.322102231125314
				],
				[
					21.026816376177067,
					12.535181858541591
				],
				[
					23.452944780720372,
					13.748276911102153
				],
				[
					25.879134885841722,
					14.152631645192798
				],
				[
					28.305263290385483,
					14.96135653851843
				],
				[
					29.114034459144023,
					15.365711272609019
				],
				[
					29.922743927325428,
					15.365711272609019
				],
				[
					31.135838979886103,
					15.365711272609019
				],
				[
					31.540162863687783,
					15.365711272609019
				],
				[
					32.34887233186919,
					15.365711272609019
				],
				[
					32.75325791624846,
					15.365711272609019
				],
				[
					33.15764350062773,
					15.365711272609019
				],
				[
					35.17944802136981,
					15.365711272609019
				],
				[
					35.58377190517149,
					15.365711272609019
				],
				[
					38.00996201029284,
					16.174436165934594
				],
				[
					39.22305706285306,
					16.174436165934594
				],
				[
					40.84047599921587,
					16.174436165934594
				],
				[
					42.457894935578224,
					16.174436165934594
				],
				[
					43.6709899881389,
					16.57879090002524
				],
				[
					44.884085040699574,
					16.57879090002524
				],
				[
					46.097180093259794,
					16.57879090002524
				],
				[
					46.50150397706193,
					16.57879090002524
				],
				[
					47.714599029622605,
					16.57879090002524
				],
				[
					48.118984614001874,
					16.57879090002524
				],
				[
					49.33207966656255,
					17.38751579335087
				],
				[
					51.353884187304175,
					17.38751579335087
				],
				[
					52.16259365548558,
					17.791885952585858
				],
				[
					53.375688708046255,
					17.791885952585858
				],
				[
					54.99310764440861,
					17.791885952585858
				],
				[
					55.801817112590015,
					17.791885952585858
				],
				[
					56.206202696969285,
					17.791885952585858
				],
				[
					57.01491216515069,
					17.791885952585858
				],
				[
					57.41929774952996,
					17.791885952585858
				],
				[
					58.22800721771091,
					17.791885952585858
				],
				[
					58.632331101513046,
					17.791885952585858
				],
				[
					59.036716685892316,
					17.791885952585858
				],
				[
					59.84542615407372,
					17.791885952585858
				],
				[
					60.24981173845299,
					17.791885952585858
				],
				[
					61.05852120663394,
					17.791885952585858
				],
				[
					61.46290679101321,
					17.791885952585858
				],
				[
					62.271616259194616,
					17.791885952585858
				],
				[
					62.67594014299675,
					17.791885952585858
				],
				[
					63.08032572737602,
					17.791885952585858
				],
				[
					63.08032572737602,
					18.196240686676447
				],
				[
					63.08032572737602,
					19.409320314092724
				],
				[
					63.08032572737602,
					20.2180452074183
				],
				[
					63.08032572737602,
					20.62239994150889
				],
				[
					63.08032572737602,
					21.026770100743875
				],
				[
					62.67594014299675,
					21.83549499406945
				],
				[
					62.67594014299675,
					22.239849728160152
				],
				[
					62.67594014299675,
					23.048574621485727
				],
				[
					62.67594014299675,
					23.452929355576316
				],
				[
					62.67594014299675,
					24.26165424890189
				],
				[
					62.67594014299675,
					24.666008982992594
				],
				[
					62.67594014299675,
					25.07037914222758
				],
				[
					62.67594014299675,
					25.879104035553155
				],
				[
					62.67594014299675,
					26.283458769643744
				],
				[
					61.867230674815346,
					27.092183662969433
				],
				[
					61.867230674815346,
					27.49653839706002
				],
				[
					61.867230674815346,
					28.305263290385597
				],
				[
					61.46290679101321,
					28.305263290385597
				],
				[
					61.46290679101321,
					28.7096180244763
				],
				[
					60.65413562225467,
					28.7096180244763
				],
				[
					60.65413562225467,
					29.113988183711285
				],
				[
					60.24981173845299,
					29.113988183711285
				],
				[
					59.441102270271585,
					29.113988183711285
				],
				[
					59.036716685892316,
					29.113988183711285
				],
				[
					58.632331101513046,
					29.113988183711285
				],
				[
					58.632331101513046,
					28.7096180244763
				],
				[
					57.82362163333164,
					28.7096180244763
				],
				[
					57.41929774952996,
					27.900908556295008
				],
				[
					56.61052658077142,
					27.49653839706002
				],
				[
					56.206202696969285,
					27.49653839706002
				],
				[
					55.39749322878788,
					26.687813503734446
				],
				[
					54.99310764440861,
					26.283458769643744
				],
				[
					54.58872206002934,
					26.283458769643744
				],
				[
					54.58872206002934,
					25.47473387631817
				],
				[
					53.780012591847935,
					25.47473387631817
				],
				[
					53.780012591847935,
					25.07037914222758
				],
				[
					53.375688708046255,
					25.07037914222758
				],
				[
					54.184398176227205,
					25.07037914222758
				],
				[
					54.58872206002934,
					25.879104035553155
				],
				[
					54.99310764440861,
					26.283458769643744
				],
				[
					55.801817112590015,
					26.283458769643744
				],
				[
					56.206202696969285,
					27.092183662969433
				],
				[
					56.206202696969285,
					27.49653839706002
				],
				[
					57.01491216515069,
					27.49653839706002
				],
				[
					57.01491216515069,
					28.305263290385597
				],
				[
					57.41929774952996,
					28.305263290385597
				],
				[
					58.22800721771091,
					28.7096180244763
				],
				[
					58.22800721771091,
					29.113988183711285
				],
				[
					58.632331101513046,
					29.92271307703686
				],
				[
					59.036716685892316,
					29.92271307703686
				],
				[
					59.036716685892316,
					30.32706781112745
				],
				[
					59.84542615407372,
					30.32706781112745
				],
				[
					60.24981173845299,
					31.135792704453024
				],
				[
					61.05852120663394,
					31.135792704453024
				],
				[
					61.05852120663394,
					31.540147438543613
				],
				[
					61.46290679101321,
					31.540147438543613
				],
				[
					62.271616259194616,
					31.540147438543613
				],
				[
					62.67594014299675,
					31.540147438543613
				],
				[
					62.67594014299675,
					30.731422545218038
				],
				[
					63.08032572737602,
					30.32706781112745
				],
				[
					63.889035195557426,
					29.518342917801874
				],
				[
					64.2934207799367,
					29.113988183711285
				],
				[
					65.10213024811765,
					28.7096180244763
				],
				[
					65.50651583249737,
					28.7096180244763
				],
				[
					65.91083971629905,
					27.900908556295008
				],
				[
					66.71954918448046,
					27.900908556295008
				],
				[
					66.71954918448046,
					27.49653839706002
				],
				[
					67.12393476885973,
					27.49653839706002
				],
				[
					67.12393476885973,
					27.49653839706002
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 113,
			"versionNonce": 1232422589,
			"isDeleted": false,
			"id": "4RYK03pPXpLeNukZqOc6K",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2484.212383801956,
			"y": 558.4681406118139,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 16.17443616593482,
			"height": 20.2180452074183,
			"seed": 509686707,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-0.40435473409070255,
					0.40435473409058886
				],
				[
					-0.40435473409070255,
					0.8087403184699724
				],
				[
					-1.213095052560675,
					1.2130950525605613
				],
				[
					-1.6174497866513775,
					2.0218045207418527
				],
				[
					-2.02180452074208,
					2.4261592548324415
				],
				[
					-2.8305448392120525,
					3.234899573302414
				],
				[
					-3.234899573302755,
					3.639254307393003
				],
				[
					-4.043609041483705,
					4.852349359953564
				],
				[
					-4.447963775574408,
					5.256704094044153
				],
				[
					-5.25670409404438,
					6.065413562225444
				],
				[
					-5.661058828135083,
					6.469768296316033
				],
				[
					-6.874153880695758,
					7.278508614786006
				],
				[
					-6.874153880695758,
					7.682863348876708
				],
				[
					-7.278508614786006,
					8.087218082967297
				],
				[
					-8.08721808296741,
					8.89595840143727
				],
				[
					-8.491572817058113,
					9.300313135527858
				],
				[
					-8.491572817058113,
					10.10902260370915
				],
				[
					-8.895958401437383,
					10.10902260370915
				],
				[
					-8.895958401437383,
					10.513377337799739
				],
				[
					-9.704667869618788,
					11.322117656269711
				],
				[
					-10.10902260370949,
					11.7264723903603
				],
				[
					-10.10902260370949,
					12.130827124450889
				],
				[
					-10.10902260370949,
					12.939567442920861
				],
				[
					-10.10902260370949,
					13.343922177011564
				],
				[
					-10.917762922179463,
					13.343922177011564
				],
				[
					-10.917762922179463,
					14.152631645192741
				],
				[
					-10.917762922179463,
					14.556986379283444
				],
				[
					-11.322117656269711,
					14.556986379283444
				],
				[
					-11.322117656269711,
					15.365726697753416
				],
				[
					-12.130827124451116,
					15.365726697753416
				],
				[
					-12.130827124451116,
					15.770081431844005
				],
				[
					-12.535181858541819,
					15.770081431844005
				],
				[
					-12.939567442921089,
					15.770081431844005
				],
				[
					-13.748276911102494,
					15.770081431844005
				],
				[
					-13.748276911102494,
					14.961371963662714
				],
				[
					-14.152631645192741,
					14.556986379283444
				],
				[
					-14.152631645192741,
					13.748276911102153
				],
				[
					-14.961371963662714,
					13.343922177011564
				],
				[
					-14.961371963662714,
					12.535181858541591
				],
				[
					-15.365726697753416,
					12.130827124450889
				],
				[
					-15.365726697753416,
					11.7264723903603
				],
				[
					-16.17443616593482,
					11.7264723903603
				],
				[
					-16.17443616593482,
					10.917762922179122
				],
				[
					-16.17443616593482,
					10.513377337799739
				],
				[
					-16.17443616593482,
					9.70466786961856
				],
				[
					-16.17443616593482,
					9.300313135527858
				],
				[
					-16.17443616593482,
					8.491572817057886
				],
				[
					-15.770081431844119,
					8.89595840143727
				],
				[
					-15.770081431844119,
					9.300313135527858
				],
				[
					-15.365726697753416,
					10.10902260370915
				],
				[
					-14.556986379283444,
					10.513377337799739
				],
				[
					-14.556986379283444,
					11.322117656269711
				],
				[
					-14.152631645192741,
					12.130827124450889
				],
				[
					-14.152631645192741,
					12.939567442920861
				],
				[
					-13.343922177011791,
					14.556986379283444
				],
				[
					-12.939567442921089,
					15.365726697753416
				],
				[
					-12.535181858541819,
					16.174436165934594
				],
				[
					-12.535181858541819,
					16.983176484404567
				],
				[
					-11.726472390360414,
					17.38753121849527
				],
				[
					-11.726472390360414,
					18.196240686676447
				],
				[
					-11.322117656269711,
					18.600595420767036
				],
				[
					-11.322117656269711,
					19.00498100514642
				],
				[
					-10.513377337799739,
					19.813690473327597
				],
				[
					-10.10902260370949,
					20.2180452074183
				],
				[
					-9.300313135528086,
					20.2180452074183
				],
				[
					-8.895958401437383,
					19.409335739237008
				],
				[
					-8.895958401437383,
					19.00498100514642
				],
				[
					-8.491572817058113,
					19.00498100514642
				],
				[
					-7.682863348876708,
					18.600595420767036
				],
				[
					-7.682863348876708,
					17.791885952585858
				],
				[
					-7.278508614786006,
					17.38753121849527
				],
				[
					-7.278508614786006,
					16.578790900025297
				],
				[
					-6.469768296316033,
					16.578790900025297
				],
				[
					-6.469768296316033,
					16.174436165934594
				],
				[
					-6.065413562225785,
					16.174436165934594
				],
				[
					-5.661058828135083,
					15.770081431844005
				],
				[
					-5.661058828135083,
					14.961371963662714
				],
				[
					-5.661058828135083,
					14.961371963662714
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 121,
			"versionNonce": 678776723,
			"isDeleted": false,
			"id": "SBysH5KY2qr2-qyHCM5Ib",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2529.905178310837,
			"y": 560.085590398465,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 23.048559196341103,
			"height": 28.30526329038571,
			"seed": 994366899,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.4043238838016805,
					0
				],
				[
					0.4043238838016805,
					0.8087094681812914
				],
				[
					1.2130950525602202,
					0.8087094681812914
				],
				[
					1.2130950525602202,
					1.2130950525605613
				],
				[
					1.6174189363623555,
					1.2130950525605613
				],
				[
					2.0218045207416253,
					2.0218045207418527
				],
				[
					2.0218045207416253,
					2.4261592548324415
				],
				[
					2.8305139889230304,
					2.8305139889230304
				],
				[
					2.8305139889230304,
					3.639254307393003
				],
				[
					3.2348995733023003,
					4.852318509664883
				],
				[
					4.447932925285386,
					5.6610588281348555
				],
				[
					4.852318509664656,
					6.874123030406736
				],
				[
					6.065413562225331,
					8.08721808296741
				],
				[
					7.278508614786006,
					9.70466786961856
				],
				[
					8.491541966769091,
					10.917732071890441
				],
				[
					9.704637019329766,
					12.130827124451002
				],
				[
					10.917732071889986,
					13.343922177011564
				],
				[
					11.322117656269256,
					14.556986379283444
				],
				[
					12.535151008252797,
					14.961341113374147
				],
				[
					12.535151008252797,
					15.770081431844119
				],
				[
					12.939536592632066,
					16.174436165934708
				],
				[
					12.939536592632066,
					16.983145634115886
				],
				[
					13.748246060813472,
					17.38753121849527
				],
				[
					13.748246060813472,
					17.791885952585858
				],
				[
					14.152631645192741,
					17.791885952585858
				],
				[
					14.152631645192741,
					18.60059542076715
				],
				[
					14.152631645192741,
					19.004950154857738
				],
				[
					14.961341113373692,
					19.81369047332771
				],
				[
					14.961341113373692,
					20.2180452074183
				],
				[
					15.365726697753416,
					20.622399941509002
				],
				[
					15.365726697753416,
					21.431140259978974
				],
				[
					15.770050581555097,
					21.835494994069563
				],
				[
					15.770050581555097,
					22.644204462250855
				],
				[
					16.578760049736502,
					23.048559196341444
				],
				[
					16.578760049736502,
					23.857299514811416
				],
				[
					16.578760049736502,
					24.261654248902005
				],
				[
					16.983145634115772,
					24.666008982992594
				],
				[
					16.983145634115772,
					25.474749301462566
				],
				[
					16.983145634115772,
					25.879104035553155
				],
				[
					16.174436165934367,
					25.879104035553155
				],
				[
					15.770050581555097,
					25.879104035553155
				],
				[
					15.365726697753416,
					25.879104035553155
				],
				[
					14.556955528994422,
					25.070363717083296
				],
				[
					14.152631645192741,
					24.666008982992594
				],
				[
					13.343922177011336,
					24.261654248902005
				],
				[
					12.939536592632066,
					24.261654248902005
				],
				[
					12.535151008252797,
					23.452944780720713
				],
				[
					11.726441540071392,
					23.048559196341444
				],
				[
					11.322117656269256,
					22.239849728160152
				],
				[
					10.513346487510717,
					21.835494994069563
				],
				[
					10.109022603709036,
					21.02675467559959
				],
				[
					9.300313135527631,
					20.622399941509002
				],
				[
					9.704637019329766,
					20.622399941509002
				],
				[
					10.109022603709036,
					21.431140259978974
				],
				[
					10.917732071889986,
					21.835494994069563
				],
				[
					11.322117656269256,
					22.644204462250855
				],
				[
					12.130827124450661,
					22.644204462250855
				],
				[
					12.535151008252797,
					23.048559196341444
				],
				[
					12.939536592632066,
					23.857299514811416
				],
				[
					13.748246060813472,
					23.857299514811416
				],
				[
					13.748246060813472,
					24.261654248902005
				],
				[
					14.152631645192741,
					24.261654248902005
				],
				[
					14.152631645192741,
					24.666008982992594
				],
				[
					14.961341113373692,
					25.474749301462566
				],
				[
					15.365726697753416,
					25.879104035553155
				],
				[
					15.770050581555097,
					26.687813503734446
				],
				[
					16.578760049736502,
					27.092168237825035
				],
				[
					16.983145634115772,
					27.900908556295008
				],
				[
					17.791855102296722,
					27.900908556295008
				],
				[
					18.196240686675992,
					27.900908556295008
				],
				[
					18.196240686675992,
					28.30526329038571
				],
				[
					19.004950154857397,
					28.30526329038571
				],
				[
					19.409335739236667,
					28.30526329038571
				],
				[
					19.813659623038802,
					28.30526329038571
				],
				[
					20.622369091220207,
					28.30526329038571
				],
				[
					20.622369091220207,
					27.49655382220442
				],
				[
					21.026754675599477,
					26.283458769643858
				],
				[
					21.835464143780882,
					25.879104035553155
				],
				[
					22.239849728160152,
					25.070363717083296
				],
				[
					22.239849728160152,
					24.666008982992594
				],
				[
					22.239849728160152,
					24.261654248902005
				],
				[
					23.048559196341103,
					24.261654248902005
				],
				[
					23.048559196341103,
					23.452944780720713
				],
				[
					23.048559196341103,
					23.048559196341444
				],
				[
					23.048559196341103,
					22.239849728160152
				],
				[
					23.048559196341103,
					22.239849728160152
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 113,
			"versionNonce": 1073178397,
			"isDeleted": false,
			"id": "dx3b72bIZYUnmm9s2-YZ0",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2444.989357589391,
			"y": 617.9092120317969,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 12.939567442921089,
			"height": 23.048559196341444,
			"seed": 1537954995,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.8087094681812914
				],
				[
					0,
					1.2130642022718803
				],
				[
					0,
					2.0218045207418527
				],
				[
					0,
					2.4261592548325552
				],
				[
					0,
					2.830513988923144
				],
				[
					0,
					3.6392234571044355
				],
				[
					0,
					4.043609041483705
				],
				[
					0,
					4.852318509664883
				],
				[
					0,
					5.256673243755586
				],
				[
					0,
					6.065413562225558
				],
				[
					0,
					6.469768296316147
				],
				[
					0,
					6.874123030406736
				],
				[
					0,
					7.682832498588027
				],
				[
					0,
					8.08721808296741
				],
				[
					0,
					8.895927551148588
				],
				[
					0,
					9.300282285239291
				],
				[
					0,
					10.109022603709263
				],
				[
					0,
					10.513377337799739
				],
				[
					0,
					11.726441540071619
				],
				[
					0,
					12.130827124451002
				],
				[
					-0.40435473409070255,
					12.939536592632294
				],
				[
					-0.40435473409070255,
					13.343891326722883
				],
				[
					-0.40435473409070255,
					14.152631645192855
				],
				[
					-1.213064202271653,
					14.961341113374147
				],
				[
					-1.213064202271653,
					15.770050581555324
				],
				[
					-1.213064202271653,
					16.174436165934708
				],
				[
					-1.6174189363623555,
					16.983145634116
				],
				[
					-1.6174189363623555,
					17.387500368206588
				],
				[
					-2.426159254832328,
					18.60059542076715
				],
				[
					-2.426159254832328,
					19.004950154857852
				],
				[
					-2.8305139889230304,
					19.81365962303903
				],
				[
					-2.8305139889230304,
					20.2180452074183
				],
				[
					-2.8305139889230304,
					21.02675467559959
				],
				[
					-3.234868723013733,
					21.02675467559959
				],
				[
					-3.234868723013733,
					21.43110940969018
				],
				[
					-3.234868723013733,
					21.835464143780882
				],
				[
					-3.234868723013733,
					22.644204462250855
				],
				[
					-4.043609041483705,
					22.644204462250855
				],
				[
					-4.043609041483705,
					23.048559196341444
				],
				[
					-4.447963775574408,
					23.048559196341444
				],
				[
					-5.256673243755358,
					23.048559196341444
				],
				[
					-5.661027977846061,
					22.239849728160152
				],
				[
					-5.661027977846061,
					21.835464143780882
				],
				[
					-6.469768296316033,
					21.43110940969018
				],
				[
					-6.874123030406736,
					20.622399941509002
				],
				[
					-6.874123030406736,
					20.2180452074183
				],
				[
					-7.278477764497438,
					19.409304888948327
				],
				[
					-8.08721808296741,
					19.004950154857852
				],
				[
					-8.08721808296741,
					18.196240686676447
				],
				[
					-8.08721808296741,
					17.791855102297177
				],
				[
					-8.08721808296741,
					17.387500368206588
				],
				[
					-8.08721808296741,
					16.578790900025297
				],
				[
					-7.682832498588141,
					16.983145634116
				],
				[
					-7.278477764497438,
					17.387500368206588
				],
				[
					-6.874123030406736,
					17.387500368206588
				],
				[
					-6.065413562225331,
					17.791855102297177
				],
				[
					-6.065413562225331,
					18.60059542076715
				],
				[
					-5.661027977846061,
					18.60059542076715
				],
				[
					-4.852318509664656,
					19.004950154857852
				],
				[
					-4.447963775574408,
					19.81365962303903
				],
				[
					-3.6392234571044355,
					19.81365962303903
				],
				[
					-3.234868723013733,
					20.2180452074183
				],
				[
					-2.8305139889230304,
					21.02675467559959
				],
				[
					-2.0218045207416253,
					21.43110940969018
				],
				[
					-1.6174189363623555,
					21.43110940969018
				],
				[
					-0.8087094681814051,
					20.622399941509002
				],
				[
					-0.40435473409070255,
					19.409304888948327
				],
				[
					0,
					18.196240686676447
				],
				[
					0.8087403184699724,
					17.387500368206588
				],
				[
					2.02180452074208,
					16.578790900025297
				],
				[
					2.42619010512135,
					15.365695847464735
				],
				[
					3.2348995733023003,
					14.961341113374147
				],
				[
					3.639254307393003,
					14.556986379283444
				],
				[
					3.639254307393003,
					13.748246060813472
				],
				[
					4.043609041483705,
					13.748246060813472
				],
				[
					4.043609041483705,
					13.343891326722883
				],
				[
					4.852349359953678,
					13.343891326722883
				],
				[
					4.852349359953678,
					13.343891326722883
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 112,
			"versionNonce": 1793844531,
			"isDeleted": false,
			"id": "dzcqZ66MaTxcgmMpByz4V",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2480.1687747604724,
			"y": 619.1222762340687,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 31.94448674748992,
			"height": 24.666008982992707,
			"seed": 337966771,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.40435473409070255,
					0
				],
				[
					1.6174497866509228,
					0
				],
				[
					2.0218045207416253,
					0.8087403184699724
				],
				[
					2.8305139889230304,
					1.213095052560675
				],
				[
					3.234868723013733,
					1.213095052560675
				],
				[
					3.234868723013733,
					1.6174497866512638
				],
				[
					4.447963775574408,
					2.4261592548325552
				],
				[
					5.661058828134628,
					3.639254307393003
				],
				[
					6.874123030406736,
					4.852349359953678
				],
				[
					8.08721808296741,
					5.6610588281348555
				],
				[
					10.917732071890441,
					7.682863348876708
				],
				[
					13.343891326722769,
					9.300313135527858
				],
				[
					15.770050581555097,
					11.322117656269711
				],
				[
					18.196240686676447,
					12.535181858541591
				],
				[
					19.813659623038802,
					14.152631645192855
				],
				[
					21.835464143780882,
					14.556986379283444
				],
				[
					22.239849728160152,
					15.365726697753416
				],
				[
					23.452944780720827,
					15.770081431844119
				],
				[
					24.666039833281047,
					16.578790900025297
				],
				[
					25.879073185264588,
					16.983176484404567
				],
				[
					26.283458769643858,
					17.79188595258597
				],
				[
					27.092168237824808,
					18.196240686676447
				],
				[
					27.496553822204532,
					18.196240686676447
				],
				[
					27.496553822204532,
					18.60059542076715
				],
				[
					27.900877706006213,
					18.60059542076715
				],
				[
					27.900877706006213,
					19.40933573923712
				],
				[
					27.496553822204532,
					19.00498100514642
				],
				[
					26.687844354023127,
					18.60059542076715
				],
				[
					25.474749301462452,
					18.196240686676447
				],
				[
					25.474749301462452,
					17.38753121849527
				],
				[
					25.070363717083183,
					17.38753121849527
				],
				[
					24.261654248901777,
					16.983176484404567
				],
				[
					23.857268664522508,
					16.174436165934708
				],
				[
					23.452944780720827,
					16.174436165934708
				],
				[
					23.452944780720827,
					15.770081431844119
				],
				[
					22.644235312539422,
					15.770081431844119
				],
				[
					22.239849728160152,
					15.770081431844119
				],
				[
					22.239849728160152,
					14.961371963662828
				],
				[
					21.431140259978747,
					14.961371963662828
				],
				[
					21.431140259978747,
					15.365726697753416
				],
				[
					21.835464143780882,
					15.770081431844119
				],
				[
					21.835464143780882,
					16.578790900025297
				],
				[
					22.239849728160152,
					16.983176484404567
				],
				[
					23.048559196341103,
					17.79188595258597
				],
				[
					23.452944780720827,
					18.196240686676447
				],
				[
					23.857268664522508,
					18.60059542076715
				],
				[
					24.666039833281047,
					19.40933573923712
				],
				[
					25.070363717083183,
					19.81369047332771
				],
				[
					26.283458769643858,
					20.622399941509002
				],
				[
					27.092168237824808,
					21.026785525888272
				],
				[
					27.496553822204532,
					21.835494994069563
				],
				[
					28.709648874764753,
					22.239849728160152
				],
				[
					29.113972758566888,
					22.644204462250855
				],
				[
					29.92268222674784,
					23.452944780720827
				],
				[
					30.327067811127563,
					23.452944780720827
				],
				[
					30.731453395506833,
					23.857299514811416
				],
				[
					31.540162863687783,
					24.666008982992707
				],
				[
					31.94448674748992,
					24.666008982992707
				],
				[
					31.94448674748992,
					24.261654248902005
				],
				[
					31.94448674748992,
					23.857299514811416
				],
				[
					31.94448674748992,
					22.644204462250855
				],
				[
					31.94448674748992,
					22.239849728160152
				],
				[
					31.94448674748992,
					21.431140259978974
				],
				[
					31.135777279308513,
					21.026785525888272
				],
				[
					31.135777279308513,
					20.2180452074183
				],
				[
					30.731453395506833,
					19.81369047332771
				],
				[
					30.731453395506833,
					19.00498100514642
				],
				[
					30.731453395506833,
					18.60059542076715
				],
				[
					30.327067811127563,
					18.196240686676447
				],
				[
					30.327067811127563,
					17.38753121849527
				],
				[
					29.518358342946158,
					16.983176484404567
				],
				[
					29.518358342946158,
					16.174436165934708
				],
				[
					29.518358342946158,
					15.770081431844119
				],
				[
					29.518358342946158,
					14.961371963662828
				],
				[
					29.518358342946158,
					14.556986379283444
				],
				[
					29.92268222674784,
					14.556986379283444
				],
				[
					29.92268222674784,
					14.556986379283444
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 103,
			"versionNonce": 352474365,
			"isDeleted": false,
			"id": "2BAxlGG0NItW3Wx51kuQQ",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2672.3897094928006,
			"y": 495.5552545430503,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 18.981904958807718,
			"height": 36.77741445814695,
			"seed": 543099197,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158219,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.7909152208591195
				],
				[
					0,
					1.1863652885621718
				],
				[
					0,
					1.9772805094213481
				],
				[
					0,
					2.3727305771243437
				],
				[
					0,
					2.7681957302805245
				],
				[
					0,
					4.745476239701929
				],
				[
					-0.3954802386092524,
					5.931856613717173
				],
				[
					-0.3954802386092524,
					6.722756749123278
				],
				[
					-1.1863803740152434,
					8.700037258544626
				],
				[
					-1.1863803740152434,
					9.886417632559983
				],
				[
					-1.1863803740152434,
					11.468217903372079
				],
				[
					-1.1863803740152434,
					13.050048345090431
				],
				[
					-1.5818606126244958,
					14.631878786808784
				],
				[
					-1.5818606126244958,
					16.609159296230132
				],
				[
					-2.372760748030487,
					18.190989737948485
				],
				[
					-2.372760748030487,
					19.772820179666837
				],
				[
					-2.372760748030487,
					20.959170382775937
				],
				[
					-2.372760748030487,
					22.14555075679118
				],
				[
					-2.7681806448272255,
					23.33190095990028
				],
				[
					-2.7681806448272255,
					23.727381198509534
				],
				[
					-2.7681806448272255,
					24.51828133391564
				],
				[
					-3.5591411220457303,
					24.913731401618634
				],
				[
					-3.5591411220457303,
					25.30918146932163
				],
				[
					-3.5591411220457303,
					26.10011177563399
				],
				[
					-3.954561018842469,
					26.10011177563399
				],
				[
					-3.954561018842469,
					25.70466170793088
				],
				[
					-4.350041257452176,
					25.70466170793088
				],
				[
					-5.140941392858167,
					25.70466170793088
				],
				[
					-5.5364216314674195,
					25.30918146932163
				],
				[
					-6.3273217668734105,
					24.913731401618634
				],
				[
					-6.722741663670149,
					24.122831266212643
				],
				[
					-8.304602276294645,
					22.936450892197286
				],
				[
					-9.490982650309888,
					22.541000824494176
				],
				[
					-10.677302682513073,
					21.354620450478933
				],
				[
					-11.863683056528316,
					20.168270247369833
				],
				[
					-13.05006343054356,
					19.772820179666837
				],
				[
					-13.445513498246328,
					18.981889873354476
				],
				[
					-13.445513498246328,
					18.58643980565148
				],
				[
					-14.236443804558803,
					18.58643980565148
				],
				[
					-14.236443804558803,
					17.79553967024549
				],
				[
					-13.84099373685558,
					17.79553967024549
				],
				[
					-13.445513498246328,
					18.190989737948485
				],
				[
					-12.654613362840337,
					18.58643980565148
				],
				[
					-12.259163295137569,
					19.772820179666837
				],
				[
					-11.468263159731578,
					20.563720315072942
				],
				[
					-10.677302682513073,
					21.354620450478933
				],
				[
					-9.886402547106627,
					23.33190095990028
				],
				[
					-9.490982650309888,
					24.51828133391564
				],
				[
					-8.700022173091384,
					26.10011177563399
				],
				[
					-7.513702140888654,
					27.681942217352344
				],
				[
					-6.722741663670149,
					29.65922272677369
				],
				[
					-5.5364216314674195,
					30.450122862179796
				],
				[
					-4.350041257452176,
					32.427403371601144
				],
				[
					-3.163660883436478,
					33.61378374561639
				],
				[
					-1.9772805094212345,
					34.40468388102249
				],
				[
					-0.790900135405991,
					35.591064255037736
				],
				[
					-0.3954802386092524,
					36.38196439044384
				],
				[
					0.3954198967967386,
					36.38196439044384
				],
				[
					0.3954198967967386,
					36.77741445814695
				],
				[
					0.790900135405991,
					36.77741445814695
				],
				[
					1.1863803740152434,
					36.77741445814695
				],
				[
					1.9772805094216892,
					36.77741445814695
				],
				[
					1.9772805094216892,
					35.986514322740845
				],
				[
					2.372700406218428,
					35.591064255037736
				],
				[
					3.1636608834369326,
					34.40468388102249
				],
				[
					3.1636608834369326,
					34.0092338133195
				],
				[
					3.5590807802336712,
					32.82285343930414
				],
				[
					3.5590807802336712,
					32.031953303898035
				],
				[
					4.349980915639662,
					30.450122862179796
				],
				[
					4.349980915639662,
					30.054672794476687
				],
				[
					4.349980915639662,
					29.26374248816444
				],
				[
					4.745461154248915,
					28.86829242046133
				],
				[
					4.745461154248915,
					28.07739228505534
				],
				[
					4.745461154248915,
					27.681942217352344
				],
				[
					4.745461154248915,
					26.891011911039982
				],
				[
					4.745461154248915,
					26.891011911039982
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "freedraw",
			"version": 133,
			"versionNonce": 1810168253,
			"isDeleted": false,
			"id": "3Xjyl9rRfl9hVJGepMSox",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2723.0081026023504,
			"y": 498.3234502733308,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 18.190944481589213,
			"height": 26.495546757883915,
			"seed": 480898717,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158220,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.790900135405991,
					0
				],
				[
					0.790900135405991,
					0.39545006770305235
				],
				[
					1.1863200322027296,
					0.39545006770305235
				],
				[
					1.1863200322027296,
					1.1863652885621718
				],
				[
					1.9772805094212345,
					1.5818153562652242
				],
				[
					2.372700406217973,
					2.3727305771244005
				],
				[
					2.372700406217973,
					2.768180644827396
				],
				[
					3.163600541624419,
					3.954561018842753
				],
				[
					3.163600541624419,
					4.350011086545749
				],
				[
					3.5590807802332165,
					5.140941392858053
				],
				[
					3.5590807802332165,
					5.536391460561106
				],
				[
					3.9545610188429237,
					6.327291595967154
				],
				[
					4.74546115424846,
					6.722741663670206
				],
				[
					4.74546115424846,
					7.118221902279458
				],
				[
					5.931841528264158,
					9.095502411700807
				],
				[
					6.327261425060897,
					9.490952479403802
				],
				[
					6.722741663670149,
					10.677302682512902
				],
				[
					7.51364179907614,
					11.072782921122155
				],
				[
					7.909122037685393,
					12.259133124231255
				],
				[
					8.700022173091384,
					13.445513498246612
				],
				[
					9.095442069888577,
					14.236413633652603
				],
				[
					9.886402547106627,
					15.027343939964965
				],
				[
					10.28182244390382,
					16.21369414307395
				],
				[
					11.468202817919064,
					17.40007451708931
				],
				[
					11.468202817919064,
					18.58642472019841
				],
				[
					11.863683056528316,
					18.98190495880766
				],
				[
					12.654583191934307,
					19.772805094213652
				],
				[
					12.654583191934307,
					20.16825516191676
				],
				[
					13.050003088731046,
					20.95918546822901
				],
				[
					13.84096356594955,
					21.35463553593212
				],
				[
					13.84096356594955,
					21.750085603635114
				],
				[
					14.23638346274629,
					22.540985739041105
				],
				[
					14.23638346274629,
					22.936465977650357
				],
				[
					14.631863701355542,
					22.936465977650357
				],
				[
					14.631863701355542,
					23.727366113056462
				],
				[
					15.422763836761533,
					23.727366113056462
				],
				[
					15.422763836761533,
					24.122816180759457
				],
				[
					15.818244075370785,
					24.91374648707182
				],
				[
					15.818244075370785,
					25.309196554774815
				],
				[
					16.609144210776776,
					25.309196554774815
				],
				[
					16.609144210776776,
					25.70464662247781
				],
				[
					17.004564107573515,
					25.70464662247781
				],
				[
					17.004564107573515,
					26.495546757883915
				],
				[
					16.21366397216798,
					26.100096690180806
				],
				[
					15.818244075370785,
					25.70464662247781
				],
				[
					15.02728359815228,
					25.70464662247781
				],
				[
					14.631863701355542,
					25.309196554774815
				],
				[
					13.445483327340298,
					24.518266248462567
				],
				[
					13.050003088731046,
					24.122816180759457
				],
				[
					11.863683056528316,
					23.331916045353466
				],
				[
					10.677302682512618,
					22.936465977650357
				],
				[
					10.28182244390382,
					22.14553567133811
				],
				[
					9.490922308497375,
					22.14553567133811
				],
				[
					9.095442069888577,
					22.14553567133811
				],
				[
					9.095442069888577,
					21.750085603635114
				],
				[
					8.304541934482131,
					21.750085603635114
				],
				[
					8.304541934482131,
					21.35463553593212
				],
				[
					7.909122037685393,
					21.35463553593212
				],
				[
					7.118161560466888,
					21.35463553593212
				],
				[
					6.722741663670149,
					21.35463553593212
				],
				[
					6.722741663670149,
					20.563705229619757
				],
				[
					6.327261425060897,
					20.563705229619757
				],
				[
					5.536361289654906,
					20.16825516191676
				],
				[
					5.140881051045653,
					20.16825516191676
				],
				[
					4.349980915639662,
					20.16825516191676
				],
				[
					4.74546115424846,
					20.16825516191676
				],
				[
					5.140881051045653,
					20.16825516191676
				],
				[
					5.931841528264158,
					20.16825516191676
				],
				[
					6.327261425060897,
					20.16825516191676
				],
				[
					6.722741663670149,
					20.95918546822901
				],
				[
					7.909122037685393,
					21.35463553593212
				],
				[
					8.700022173091384,
					21.35463553593212
				],
				[
					8.700022173091384,
					21.750085603635114
				],
				[
					9.095442069888577,
					21.750085603635114
				],
				[
					9.886402547106627,
					22.540985739041105
				],
				[
					10.28182244390382,
					22.540985739041105
				],
				[
					10.677302682512618,
					22.540985739041105
				],
				[
					10.677302682512618,
					22.936465977650357
				],
				[
					11.468202817919064,
					22.936465977650357
				],
				[
					11.863683056528316,
					23.727366113056462
				],
				[
					12.654583191934307,
					24.122816180759457
				],
				[
					13.84096356594955,
					24.122816180759457
				],
				[
					13.84096356594955,
					24.91374648707182
				],
				[
					14.631863701355542,
					25.309196554774815
				],
				[
					15.422763836761533,
					25.70464662247781
				],
				[
					15.818244075370785,
					25.70464662247781
				],
				[
					16.609144210776776,
					25.70464662247781
				],
				[
					16.609144210776776,
					26.495546757883915
				],
				[
					17.004564107573515,
					26.495546757883915
				],
				[
					17.400044346183222,
					26.495546757883915
				],
				[
					18.190944481589213,
					26.495546757883915
				],
				[
					18.190944481589213,
					26.100096690180806
				],
				[
					18.190944481589213,
					25.70464662247781
				],
				[
					18.190944481589213,
					25.309196554774815
				],
				[
					18.190944481589213,
					24.518266248462567
				],
				[
					18.190944481589213,
					24.122816180759457
				],
				[
					18.190944481589213,
					23.331916045353466
				],
				[
					18.190944481589213,
					22.936465977650357
				],
				[
					18.190944481589213,
					22.14553567133811
				],
				[
					18.190944481589213,
					21.750085603635114
				],
				[
					18.190944481589213,
					21.35463553593212
				],
				[
					18.190944481589213,
					20.563705229619757
				],
				[
					18.190944481589213,
					20.16825516191676
				],
				[
					18.190944481589213,
					19.377355026510656
				],
				[
					18.190944481589213,
					18.98190495880766
				],
				[
					18.190944481589213,
					18.190974652495413
				],
				[
					18.190944481589213,
					17.795524584792417
				],
				[
					18.190944481589213,
					17.40007451708931
				],
				[
					18.190944481589213,
					17.40007451708931
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 141,
			"versionNonce": 2067205405,
			"isDeleted": false,
			"id": "cqcgUhMi",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2744.948996070148,
			"y": 438.9483783209434,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 32.8382568359375,
			"height": 17.44441009892929,
			"seed": 1681222493,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421158220,
			"link": null,
			"locked": false,
			"fontSize": 13.95552807914343,
			"fontFamily": 1,
			"text": "pivot",
			"rawText": "pivot",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "pivot",
			"lineHeight": 1.25
		},
		{
			"type": "freedraw",
			"version": 103,
			"versionNonce": 1000719293,
			"isDeleted": false,
			"id": "c6SMrW0xAADlJqXY1v6a7",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"angle": 0,
			"x": 2723.9876340005244,
			"y": 430.9577004339789,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 35.51216966028642,
			"height": 11.044457904396324,
			"seed": 753746131,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421159548,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.3398242885950822,
					0
				],
				[
					0.6796485771901644,
					0
				],
				[
					1.5292222621437759,
					0
				],
				[
					2.2088838027998463,
					0
				],
				[
					3.7381190284095283,
					0
				],
				[
					5.7770906869118335,
					0
				],
				[
					7.81607530887959,
					0
				],
				[
					10.194884219442883,
					-0.16991214429759793
				],
				[
					12.57368016654027,
					-0.339824288595139
				],
				[
					15.292326329164098,
					-0.6796550589231742
				],
				[
					17.671122276261485,
					-0.6796550589231742
				],
				[
					20.04993118682478,
					-1.0194858292511526
				],
				[
					22.428740097387617,
					-1.0194858292511526
				],
				[
					24.12788746729484,
					-1.359316599579131
				],
				[
					25.48721054860698,
					-1.359316599579131
				],
				[
					26.166859125797146,
					-1.359316599579131
				],
				[
					26.676608522155675,
					-1.529228743876729
				],
				[
					26.846520666453216,
					-1.529228743876729
				],
				[
					26.846520666453216,
					-1.6991473699071094
				],
				[
					27.186357918514204,
					-1.6991473699071094
				],
				[
					27.356270062811745,
					-1.6991473699071094
				],
				[
					27.696094351406828,
					-1.6991473699071094
				],
				[
					27.86600649570437,
					-1.529228743876729
				],
				[
					28.035931603467816,
					-1.529228743876729
				],
				[
					28.375755892062898,
					-1.1893979735487505
				],
				[
					28.54566803636044,
					-1.0194858292511526
				],
				[
					28.885505288421427,
					-0.6796550589231742
				],
				[
					29.05541743271897,
					-0.5097429146255763
				],
				[
					29.56515386561159,
					0
				],
				[
					29.735078973374584,
					0.5097493963584157
				],
				[
					30.07490326197012,
					1.019492310983992
				],
				[
					30.244815406267662,
					1.3593230813119703
				],
				[
					30.754564802625737,
					2.208896766265525
				],
				[
					31.094389091221274,
					2.7186396808911013
				],
				[
					31.264301235518815,
					3.3982947398142755
				],
				[
					31.434226343281807,
					3.908044136172691
				],
				[
					31.77405063187689,
					4.417787050798211
				],
				[
					31.94396277617443,
					4.757617821126246
				],
				[
					32.28380002823542,
					5.267360735751822
				],
				[
					32.45371217253296,
					5.777103650377342
				],
				[
					32.45371217253296,
					6.286846565002918
				],
				[
					32.6236243168305,
					6.796589479628494
				],
				[
					32.96344860542558,
					7.30633887598691
				],
				[
					33.13337371318903,
					7.646163164582106
				],
				[
					33.13337371318903,
					8.155912560940465
				],
				[
					33.47319800178411,
					8.49573684953566
				],
				[
					33.47319800178411,
					8.66565547556604
				],
				[
					33.47319800178411,
					9.00548624589402
				],
				[
					33.64311014608165,
					9.175398390191617
				],
				[
					33.64311014608165,
					9.345310534489215
				],
				[
					33.30328585748657,
					9.175398390191617
				],
				[
					33.13337371318903,
					9.175398390191617
				],
				[
					32.79353646112804,
					8.835567619863639
				],
				[
					32.45371217253296,
					8.66565547556604
				],
				[
					31.94396277617443,
					8.325824705238063
				],
				[
					30.924476946923733,
					7.816081790612486
				],
				[
					29.904991117672125,
					7.1364202499565295
				],
				[
					28.885505288421427,
					6.626677335330953
				],
				[
					28.71558018065798,
					6.456765191033355
				],
				[
					28.035931603467816,
					6.116934420705377
				],
				[
					27.186357918514204,
					5.94701579467494
				],
				[
					26.676608522155675,
					5.6071915060798005
				],
				[
					26.336784233560593,
					5.437272880049363
				],
				[
					25.827034837202063,
					5.267360735751822
				],
				[
					25.48721054860698,
					5.267360735751822
				],
				[
					25.317285440843534,
					4.927529965423787
				],
				[
					25.657122692904522,
					5.097442109721385
				],
				[
					25.827034837202063,
					5.267360735751822
				],
				[
					26.506696377858134,
					5.437272880049363
				],
				[
					27.356270062811745,
					5.94701579467494
				],
				[
					28.035931603467816,
					6.456765191033355
				],
				[
					28.71558018065798,
					6.796589479628494
				],
				[
					29.56515386561159,
					7.1364202499565295
				],
				[
					30.244815406267662,
					7.476251020284508
				],
				[
					30.754564802625737,
					7.646163164582106
				],
				[
					30.924476946923733,
					7.985993934910084
				],
				[
					31.264301235518815,
					7.985993934910084
				],
				[
					31.434226343281807,
					8.155912560940465
				],
				[
					31.77405063187689,
					8.155912560940465
				],
				[
					31.94396277617443,
					8.49573684953566
				],
				[
					32.113874920472426,
					8.49573684953566
				],
				[
					32.113874920472426,
					8.66565547556604
				],
				[
					32.45371217253296,
					8.66565547556604
				],
				[
					32.6236243168305,
					8.835567619863639
				],
				[
					32.96344860542558,
					8.835567619863639
				],
				[
					33.13337371318903,
					8.835567619863639
				],
				[
					33.30328585748657,
					8.835567619863639
				],
				[
					33.64311014608165,
					8.66565547556604
				],
				[
					34.15285954244018,
					8.155912560940465
				],
				[
					34.322771686737724,
					7.816081790612486
				],
				[
					34.662595975332806,
					7.646163164582106
				],
				[
					34.83252108309625,
					7.1364202499565295
				],
				[
					35.002433227393794,
					7.1364202499565295
				],
				[
					35.002433227393794,
					6.626677335330953
				],
				[
					35.34225751598888,
					6.626677335330953
				],
				[
					35.34225751598888,
					6.456765191033355
				],
				[
					35.51216966028642,
					6.116934420705377
				],
				[
					35.51216966028642,
					5.94701579467494
				],
				[
					35.51216966028642,
					5.6071915060798005
				],
				[
					35.51216966028642,
					5.437272880049363
				],
				[
					35.51216966028642,
					5.437272880049363
				]
			],
			"lastCommittedPoint": null,
			"simulatePressure": true,
			"pressures": []
		},
		{
			"type": "text",
			"version": 1463,
			"versionNonce": 1146546611,
			"isDeleted": false,
			"id": "lqbbIqc9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2038.1667278241584,
			"y": 347.80069511111685,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"width": 265.63189697265625,
			"height": 80,
			"seed": 602469821,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1715421234419,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "# How to pick the pivot element :\n- Random element\n- Corner element\n- middle element",
			"rawText": "# How to pick the pivot element :\n- Random element\n- Corner element\n- middle element",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "# How to pick the pivot element :\n- Random element\n- Corner element\n- middle element",
			"lineHeight": 1.25
		},
		{
			"id": "mZwLE2pl",
			"type": "text",
			"x": 2005.502404019358,
			"y": 514.7525608763007,
			"width": 359.8907165527344,
			"height": 142.96903369711708,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 0.5,
			"strokeStyle": "dashed",
			"roughness": 2,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 828848307,
			"version": 325,
			"versionNonce": 1931658717,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1715421670011,
			"link": null,
			"locked": false,
			"text": "Notes :\n- Not stable\n- In-plane\n- Merge Sort is better for linked list\n    due to memory allocation of linked\n    list is not continuous. ",
			"rawText": "Notes :\n- Not stable\n- In-plane\n- Merge Sort is better for linked list\n    due to memory allocation of linked\n    list is not continuous. ",
			"fontSize": 19.062537826282277,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Notes :\n- Not stable\n- In-plane\n- Merge Sort is better for linked list\n    due to memory allocation of linked\n    list is not continuous. ",
			"lineHeight": 1.25
		}
	],
	"appState": {
		"theme": "dark",
		"viewBackgroundColor": "#f8f9fa",
		"currentItemStrokeColor": "#1971c2",
		"currentItemBackgroundColor": "transparent",
		"currentItemFillStyle": "solid",
		"currentItemStrokeWidth": 0.5,
		"currentItemStrokeStyle": "dashed",
		"currentItemRoughness": 2,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 20,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": -1079.4245898734948,
		"scrollY": 18.820050227285208,
		"zoom": {
			"value": 0.7490902649735021
		},
		"currentItemRoundness": "round",
		"gridSize": null,
		"gridColor": {
			"Bold": "#BAC3CDFF",
			"Regular": "#E3E7EBFF"
		},
		"currentStrokeOptions": null,
		"previousGridSize": null,
		"frameRendering": {
			"enabled": true,
			"clip": true,
			"name": true,
			"outline": true
		}
	},
	"files": {}
}
```
%%