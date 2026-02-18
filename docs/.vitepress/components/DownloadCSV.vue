<script setup>
function downloadCSV() {
  const table = document.querySelector('table')
  if (!table) return

  const rows = [...table.querySelectorAll('tr')]
  const csv = rows
    .map((row) =>
      [...row.querySelectorAll('th, td')]
        .map((cell) => `"${cell.textContent.trim().replace(/"/g, '""')}"`)
        .join(',')
    )
    .join('\n')

  const blob = new Blob(['\uFEFF' + csv], {
    type: 'text/csv;charset=utf-8;',
  })
  const link = document.createElement('a')
  link.href = URL.createObjectURL(blob)
  link.download = 'mock-responses-techgrowth.csv'
  link.click()
  URL.revokeObjectURL(link.href)
}
</script>

<template>
  <button class="download-btn" @click="downloadCSV">
    ⬇ Descargar como CSV
  </button>
</template>

<style scoped>
.download-btn {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 8px 16px;
  margin: 12px 0;
  border: 1px solid var(--vp-c-brand-1);
  border-radius: 8px;
  background: var(--vp-c-brand-soft);
  color: var(--vp-c-brand-1);
  font-weight: 600;
  font-size: 14px;
  cursor: pointer;
  transition: all 0.2s ease;
}

.download-btn:hover {
  background: var(--vp-c-brand-1);
  color: var(--vp-c-white);
}
</style>
