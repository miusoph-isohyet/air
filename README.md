# Arithmetic Intermediate Representation

<tr><td style="text-align: right">n</td><td style="text-align: right">n</td><td style="text-align: right">n</td><td style="text-align: right">12</td></tr>
<tr><td style="text-align: right">n</td><td style="text-align: right">n</td><td style="text-align: right">y</td><td style="text-align: right">10</td></tr>
<tr><td style="text-align: right">n</td><td style="text-align: right">y</td><td style="text-align: right">n</td><td style="text-align: right">11</td></tr>
<tr><td style="text-align: right">n</td><td style="text-align: right">y</td><td style="text-align: right">y</td><td style="text-align: right">3</td></tr>
<tr><td style="text-align: right">y</td><td style="text-align: right">n</td><td style="text-align: right">n</td><td style="text-align: right">6</td></tr>
<tr><td style="text-align: right">y</td><td style="text-align: right">n</td><td style="text-align: right">y</td><td style="text-align: right">0</td></tr>
<tr><td style="text-align: right">y</td><td style="text-align: right">y</td><td style="text-align: right">n</td><td style="text-align: right">4</td></tr>
<tr><td style="text-align: right">y</td><td style="text-align: right">y</td><td style="text-align: right">y</td><td style="text-align: right">0</td></tr>
</tbody>

      
   # Arithmetic Intermediate Representation
Let all household items (🪥, 🛁, etc.) be challenges, concretely evaluation points, supplied by the verifier. Let all fruit & vegetables (🥝, 🥥, etc.) be challenges, concretely weights to compress rows, supplied by the verifier. Both types of challenges are X-field elements, i.e., elements of <img src="base64"></img>.

  # Initial Constraints
The Address is 0.<br>
The IndexInChunk is 0.<br>
The indicator IsHashInputPadding is 0.<br>
The InstructionLookupServerLogDerivative is 0.<br>
PrepareChunkRunningEvaluation has absorbed Instruction with respect to challenge 🪑.<br>
SendChunkRunningEvaluation is 1.<br>
Initial Constraints as Polynomials<br>
Address<br>
IndexInChunk<br>
IsHashInputPadding<br>
InstructionLookupServerLogDerivative<br>
PrepareChunkRunningEvaluation - 🪑 - Instruction<br>
SendChunkRunningEvaluation - 1<br>
  # Consistency Constraints
The MaxMinusIndexInChunkInv is zero or the inverse of rate−1− IndexInChunk.<br>
The IndexInChunk is rate−1 or the MaxMinusIndexInChunkInv is the inverse of rate−1− IndexInChunk.<br>
Indicator IsHashInputPadding is either 0 or 1.<br>
Indicator IsTablePadding is either 0 or 1.<br>
Consistency Constraints as Polynomials<br>
(1 - MaxMinusIndexInChunkInv · (rate - 1 - IndexInChunk)) · MaxMinusIndexInChunkInv<br>
(1 - MaxMinusIndexInChunkInv · (rate - 1 - IndexInChunk)) · (rate - 1 - IndexInChunk)<br>
IsHashInputPadding · (IsHashInputPadding - 1)<br>
IsTablePadding · (IsTablePadding - 1)<br>
  # Transition Constraints
The Address increases by 1.<br>
If the IndexInChunk is not rate−1, it increases by 1. Else, the IndexInChunk in the next row is 0.<br>
The indicator IsHashInputPadding is 0 or remains unchanged.<br>
The padding indicator IsTablePadding is 0 or remains unchanged.<br>
If IsHashInputPadding is 0 in the current row and 1 in the next row, then Instruction in the next row is 1.<br>
If IsHashInputPadding is 1 in the current row then Instruction in the next row is 0.<br>
If IsHashInputPadding is 1 in the current row and IndexInChunk is rate−1 in the current row then IsTablePadding is 1 in the next row.<br>
If the current row is not a padding row, the logarithmic derivative accumulates the current row's address, the current row's instruction, and the next row's instruction with respect to challenges 🥝, 🥥, and 🫐 and indeterminate 🪥 respectively. Otherwise, it remains unchanged.<br>
If the IndexInChunk in the current row is not rate−1, then PrepareChunkRunningEvaluation absorbs the Instruction in the next row with respect to challenge 🪑. Otherwise, PrepareChunkRunningEvaluation resets and absorbs the Instruction in the next row with respect to challenge 🪑.<br>
If the next row is not a padding row and the IndexInChunk in the next row is rate−1, then SendChunkRunningEvaluation absorbs PrepareChunkRunningEvaluation in the next row with respect to variable 🪣. Otherwise, it remains unchanged.<br>

For each table, <b>up to</b> four lists containing constraints of different type are given:

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
