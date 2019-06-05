<template>
  <table width="100%">
    <tr>
      <td width="320" height="180">
        <table width="100%" height="100%" cellpadding="0" cellspacing="0">
          <tr>
            <td bgcolor="black" width="*"></td>
            <td bgcolor="yellow" width="*"></td>
            <td bgcolor="red" width="*"></td>
          </tr>
        </table>
      </td>
      <td width="*"></td>
      <td width="320" height="180">
        <table width="100%" height="100%" cellpadding="0" cellspacing="0">
          <tr>
            <td bgcolor="black"></td>
          </tr>
          <tr>
            <td bgcolor="red"></td>
          </tr>
          <tr>
            <td bgcolor="yellow"></td>
          </tr>
        </table>
      </td>

      <td width="*"></td>
      <td width="320" height="180">
        <table width="100%" height="100%" cellpadding="0" cellspacing="0">
          <tr>
            <td bgcolor="blue" width="100" height="80"></td>
            <td bgcolor="yellow" width="20"></td>
            <td bgcolor="blue" width="200"></td>
          </tr>
          <tr>
            <td bgcolor="yellow" colspan="3" height="*"></td>
          </tr>
          <tr>
            <td bgcolor="blue" width="100" height="80"></td>
            <td bgcolor="yellow" width="20"></td>
            <td bgcolor="blue" width="200"></td>
          </tr>
        </table>
      </td>
    </tr>
  </table>
</template>

<script>
export default {
  name: 'Table',
  layout: 'layouting',
}
</script>

<style lang="scss">
/* Look ma not CSS... Just like you used to make websites in the old days! */
</style>
