<script lang="ts">
export let baseAtk: number;
export let baseWpnAtk: number;

const artfactBonus = 0.0;
const elDmg = 0.466;

let healBonus = 0.359;
let hpBase = 13470;
let hpBonus = 0.466;
let hpFlatBonus = 4780;
let hp = hpBase * (1 + hpBonus) + hpFlatBonus;
let burstBonus = 	((0.0823 + (0.15 * healBonus)) * hp);7
let flatAtkBonus = 311;
let flatDmg = (baseAtk + baseWpnAtk) * (1 + artfactBonus) + burstBonus + flatAtkBonus;
let autoDmg = flatDmg * (1 + elDmg);
</script>

<table>
  <tr>
    <td>Autos</td>
    <td>{autoDmg}</td>
  </tr>
  <tr>
    <td>Elemental</td>
    <td></td>
  </tr>
  <tr>
    <td>Burst</td>
    <td></td>
  </tr>
  <tr>
    <td>Reações</td>
    <td></td>
  </tr>
</table>
