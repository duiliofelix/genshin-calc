<script lang="ts">
export let level = '1';
const specialStatName = 'Bonus Hydro DMG';

const baseAtkTable = {
  '1': 18,
  '20': 47,
  '20a': 62,
  '40': 94,
  '40a': 105,
  '50': 121,
  '50a': 136,
  '60': 152,
  '60a': 163,
  '70': 179,
  '70a': 190,
  '80': 206,
  '80a': 217,
  '90': 234,
};

let hpBase = 10;
let defBase = 10;
let spcBase = 10;

</script>
<table>
  <thead>
    <tr>
      <th>Stat</th>
      <th>Base</th>
      <th>Mod</th>
      <th>Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>hp</td>
      <td>{hpBase}</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <td>atk</td>
      <td>{baseAtkTable[level]}</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <td>def</td>
      <td>{defBase}</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <td>{specialStatName}</td>
      <td>{spcBase}</td>
      <td>1</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
