## Принимаем даты в формате Unix time
# calculateShelfLifePercentage

<pre>
// Функция для расчета процента годности продукта, принимающая даты в формате Unix time
function calculateShelfLifePercentage(productionTimestamp, shelfLifeSeconds, saleTimestamp) {
  // Рассчитываем оставшийся срок годности продукта
  const remainingShelfLife = productionTimestamp + shelfLifeSeconds - saleTimestamp;

  // Рассчитываем процент годности
  const shelfLifePercentage = (remainingShelfLife / shelfLifeSeconds) * 100;

  return shelfLifePercentage;
}

// Пример использования калькулятора с датами в формате Unix time
const productionTimestamp = 1628966400; // Дата производства в формате Unix time (в секундах с 1 января 1970 года)
const shelfLifeSeconds = 2678400; // Срок годности в секундах (31 день)
const saleTimestamp = 1662835200; // Дата продажи в формате Unix time (в секундах с 1 января 1970 года)

const percentage = calculateShelfLifePercentage(productionTimestamp, shelfLifeSeconds, saleTimestamp);
console.log(`Продукт был продан с процентом годности: ${percentage.toFixed(2)}%`);
</pre>

В этой версии функции calculateShelfLifePercentage вместо дат в формате строки принимаются временные метки Unix time (в секундах). Вы можете передавать даты в формате Unix time, как показано в примере использования.
