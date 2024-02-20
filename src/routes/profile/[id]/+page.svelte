<script lang="ts">
	import CardTable from "../../../lib/components/CardTable.svelte";
	import type { PageData } from "./$types";

	export let data: PageData;

	const { profile } = data;

	const pupil = [
		["Фамилия, имя, отчество ученика", "Филиппов Тимофей Евгеньевич"],
		["Дата рождения", "10.05.2013"],
		["Место рождения", "Г. Экибастуз"],
		["Национальность", "русский"],
		["Домашний адрес, телефон", "ул. Лихачева 24, 8 747 644 4055"],
		[
			"Состояние здоровья",
			"состоит на диспансерном\nучете у педиатра, нет\nспециальных рекомендаций\nдля организации обучения",
		],
	];

	const family = [
		["Состав семьи", "полная семья"],
		["Посещает ли ребенок кружки, секции в школе?", "Нет"],
		[
			"Посещает ли ребенок кружки, секции, клубы вне школы?",
			"Да, ребенок посещает\nфутбольную секцию в Дворце\nспорта.",
		],
		[
			"Посещает ли семья или члены семьи какие-либо религиозные\nучреждения?",
			"Нет",
		],
	];

	const father = [
		["Ф.И.О.", "Иванов Иван Иванович"],
		["Дата рождения", "01.01.1980"],
		["Образование", "высшее, инженер-механик"],
		["Должность", "главный инженер"],
		["Телефон рабочий и сотовый", "8-495-888-77-44, моб. 8-999-888-77-44"],
	];

	const mother = [
		["Ф.И.О.", "Иванова Елена Сергеевна"],
		["Дата рождения", "11.01.1982"],
		["Образование", "высшее, экономист"],
		["Место работы", 'ООО "ФинансГарант"'],
		["Должность", "финансовый аналитик"],
		["Телефон рабочий и сотовый", "8-495-888-77-44, моб. 8-999-888-77-44"],
	];
</script>

<img
	src="https://randomuser.me/api/portraits/men/45.jpg"
	class="rounded-circle flex-shrink-0 flex-grow-0 mx-auto"
	style="width: 150px; height: 150px;"
	alt="Avatar"
/>

<h1 class="display-4 text-center">Филиппов Тимофей Евгеньевич</h1>

<div class="container">
	<div class="row gx-4">
		<div class="col-md-6">
			<div class=" p-3">
				<CardTable title="Карточка ученика" data={pupil} />
			</div>
		</div>
		<div class="col-md-6">
			<div class=" p-3"><CardTable title="Семья" data={family} /></div>
		</div>
	</div>
	<div class="row gx-4">
		<div class="col-md-6">
			<div class=" p-3"><CardTable title="Отец" data={father} /></div>
		</div>
		<div class="col-md-6">
			<div class="r p-3"><CardTable title="Мать" data={mother} /></div>
		</div>
	</div>
</div>
