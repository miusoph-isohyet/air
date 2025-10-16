# Arithmetic Intermediate Representation
Let all household items (🪥, 🛁, etc. ) be challenges, concretely evaluation points, supplied by the verifier.  Let all fruit & vegetables (🥝, 🥥, etc. ) be challenges, concretely weights to compress rows, supplied by the verifier.  Both types of challenges are X-field elements, i. e. , elements of <img alt="" src="data:image/bmp;base64,Qk2mAgAAAAAAAHYAAAAoAAAAIgAAABwAAAABAAQAAAAAADACAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAgAAAgAAAAICAAIAAAACAAIAAgIAAAICAgADAwMAAAAD/AAD/AAAA//8A/wAAAP8A/wD//wAA////AP//////////////////////AAAA//////////////////////8AAAD//////////////////////wAAAP////////hzb///////////AAAA/////////3b///////////8AAAD/////////hP///////////wAAAP/////////xR3j/////////AAAA//////////NvgY////////8AAAD/////////+2/zb////////wAAAP/////////4T/tP////////AAAA/3FHFH///3gY+0d4T/+A7/8AAAD//39/////hxdzY+8e/4Bv/wAAAP//f3///////////xj/////AAAA//9/f/////////+Fj/////8AAAD//39/+I////////hf/////wAAAP//f3/zb//////3b1j/////AAAA//9/N0dv//////+Hj/////8AAAD//394gG///////////////wAAAP//f3/zf///////////////AAAA//9/f/iPj/////////////8AAAD//39///9f/////////////wAAAP//f3//90//////////////AAAA/3FHFnMEX/////////////8AAAD//////////////////////wAAAP//////////////////////AAAA//////////////////////8AAAD//////////////////////wAAAP//////////////////////AAAA" />>. 

  # Initial Constraints
1. The Address is 0. <br>
2The IndexInChunk is 0. <br>
3. The indicator IsHashInputPadding is 0. <br>
4. The InstructionLookupServerLogDerivative is 0. <br>
5. PrepareChunkRunningEvaluation has absorbed Instruction with respect to challenge 🪑. <br>
6. SendChunkRunningEvaluation is 1. <br>
7. Initial Constraints as Polynomials<br>
8. Address<br>
9. IndexInChunk<br>
10. IsHashInputPadding<br>
11. InstructionLookupServerLogDerivative<br>
12. PrepareChunkRunningEvaluation - 🪑 - Instruction<br>
13. SendChunkRunningEvaluation - 1<br>
  # Consistency Constraints
1. The MaxMinusIndexInChunkInv is zero or the inverse of rate−1− IndexInChunk. <br>
2. The IndexInChunk is rate−1 or the MaxMinusIndexInChunkInv is the inverse of rate−1− IndexInChunk. <br>
3. Indicator IsHashInputPadding is either 0 or 1. <br>
4. Indicator IsTablePadding is either 0 or 1. <br>
  # Consistency Constraints as Polynomials
1. (1 - MaxMinusIndexInChunkInv · (rate - 1 - IndexInChunk)) · MaxMinusIndexInChunkInv<br>
2. (1 - MaxMinusIndexInChunkInv · (rate - 1 - IndexInChunk)) · (rate - 1 - IndexInChunk)<br>
2. IsHashInputPadding · (IsHashInputPadding - 1)<br>
3. IsTablePadding · (IsTablePadding - 1)<br>
  # Transition Constraints
1. The Address increases by 1. <br>
2. If the IndexInChunk is not rate−1, it increases by 1.  Else, the IndexInChunk in the next row is 0. <br>
3. The indicator IsHashInputPadding is 0 or remains unchanged. <br>
4. The padding indicator IsTablePadding is 0 or remains unchanged. <br>
5. If IsHashInputPadding is 0 in the current row and 1 in the next row, then Instruction in the next row is 1. <br>
6. If IsHashInputPadding is 1 in the current row then Instruction in the next row is 0. <br>
7. If IsHashInputPadding is 1 in the current row and IndexInChunk is rate−1 in the current row then IsTablePadding is 1 in the next row. <br>
8. If the current row is not a padding row, the logarithmic derivative accumulates the current row's address, the current row's instruction, and the next row's instruction with respect to challenges 🥝, 🥥, and 🫐 and indeterminate 🪥 respectively.  Otherwise, it remains unchanged. <br>
9. If the IndexInChunk in the current row is not rate−1, then PrepareChunkRunningEvaluation absorbs the Instruction in the next row with respect to challenge 🪑.  Otherwise, PrepareChunkRunningEvaluation resets and absorbs the Instruction in the next row with respect to challenge 🪑. <br>
10. If the next row is not a padding row and the IndexInChunk in the next row is rate−1, then SendChunkRunningEvaluation absorbs PrepareChunkRunningEvaluation in the next row with respect to variable 🪣.  Otherwise, it remains unchanged. <br>

  # For each table, <b>up to</b> four lists containing constraints of different type are given:

Initial Constraints, defining values in a table's first row,
Consistency Constraints, establishing consistency within any given row,
Transition Constraints, establishing the consistency of two consecutive rows in relation to each other, and
Terminal Constraints, defining values in a table's last row. 
Together, all these constraints constitute the AIR constraints. 
   <table>   
    <thead>
     <tr>
      <th style="text-align: right">Isu3
      </th>
      <th style=text-align: right">HasArg
      </th>
      <th style="text-align: right">NumOpcodes</th>
     </tr>
   </thead>
   <tbody>
<tbody>
<tr><td style="text-align: right">n</td><td style="text-align: right">n</td><td style="text-align: right">n</td><td style="text-align: right">12</td></tr>
<tr><td style="text-align: right">n</td><td style="text-align: right">n</td><td style="text-align: right">y</td><td style="text-align: right">10</td></tr>
<tr><td style="text-align: right">n</td><td style="text-align: right">y</td><td style="text-align: right">n</td><td style="text-align: right">11</td></tr>
<tr><td style="text-align: right">n</td><td style="text-align: right">y</td><td style="text-align: right">y</td><td style="text-align: right">3</td></tr>
<tr><td style="text-align: right">y</td><td style="text-align: right">n</td><td style="text-align: right">n</td><td style="text-align: right">6</td></tr>
<tr><td style="text-align: right">y</td><td style="text-align: right">n</td><td style="text-align: right">y</td><td style="text-align: right">0</td></tr>
<tr><td style="text-align: right">y</td><td style="text-align: right">y</td><td style="text-align: right">n</td><td style="text-align: right">4</td></tr>
<tr><td style="text-align: right">y</td><td style="text-align: right">y</td><td style="text-align: right">y</td><td style="text-align: right">0</td></tr>
</tbody>
