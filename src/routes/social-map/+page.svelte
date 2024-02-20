<script lang="ts">
	import CardTable from "../../lib/components/CardTable.svelte";
	import HeaderCard from "../../lib/components/header-card.svelte";

	let socialMapData = [
		["№", "Социальные категории", "Количество", "%"],
		["1", "Полные семьи", "1500", "100%"],
		["2", "Неполные семьи", "47", "70%"],
		["3", "Нет матери", "1", "47%"],
		["4", "Нет отца", "5", "%"],
		["5", "Многодетные", "5", "%"],
		["6", "Малообеспеченные", "8", "%"],
		["7", "Сироты, дети, оставшиеся без попечения родителей", "7", "%"],
		[
			"8",
			"Дети-инвалиды, дети с особыми образовательными потребностями",
			"5",
			"%",
		],
		["9", "Учащиеся, не имеющие гражданства", "4", "%"],
		["10", "Учащиеся граждане другого государства", "5", "%"],
		["11", "Стоит на учете в отделе по делам несовершеннолетних", "0", "0%"],
		["12", "Стоит на учете внутришкольного контроля", "3", "%"],
	];
</script>

<div class="container-fluid mx-auto">
	<div class="row">
		<div class="col-md-4">
			<div class=" p-3 text-white">
				<HeaderCard>
					<svelte:fragment slot="title">Наименование школы</svelte:fragment>
					Средняя общеобразовательная школа № 44" отдела образования города Экибастуза,
					управления образования Павлодарской области
				</HeaderCard>
			</div>
		</div>
		<div class="col-md-4">
			<div class=" p-3 text-white">
				<HeaderCard>
					<svelte:fragment slot="title">БИН</svelte:fragment>
					985848449
				</HeaderCard>
			</div>
		</div>
		<div class="col-md-4">
			<div class="p-3 text-white d-flex flex-column gap-4">
				<HeaderCard>
					<svelte:fragment slot="title">Руководитель</svelte:fragment>
					Жаналиева Нургуль Сагындыковна
				</HeaderCard>
				<HeaderCard>
					<svelte:fragment slot="title"
						>Ответственный специалист</svelte:fragment
					>
					Саина Виктория
				</HeaderCard>
			</div>
		</div>
	</div>
</div>

<h1>Общее количество учащихся: 1541</h1>
<CardTable data={socialMapData} />
