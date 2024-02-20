<script>
	import "../app.scss";
	import HomeIcon from "../lib/components/icons/HomeIcon.svelte";
	import NotificationIcon from "../lib/components/icons/NotificationIcon.svelte";
</script>

<div class="d-flex vw-100 vh-100">
	<div
		class="d-flex flex-column gap-3 p-4 bg-body-secondary"
		style="width: 300px;"
	>
		<a
			href="/"
			class="d-flex flex-row gap-3 mb-4 align-items-center text-black text-decoration-none"
			style="font-size: 12px;"
		>
			<svg viewBox="0 0 100 100">
				<defs>
					<radialGradient id="grad" cx="50%" cy="50%" r="50%">
						<stop offset="0%" stop-color="black" />
						<stop offset="100%" stop-color="transparent" />
					</radialGradient>
					<linearGradient id="line-grad" x1="0%" y1="0%" x2="100%" y2="0%">
						<stop offset="0%" stop-color="white" />
						<stop offset="100%" stop-color="transparent" />
					</linearGradient>
				</defs>
				<circle cx="50%" cy="50%" r="50%" fill="url(#grad)" />
				<line
					x1="50%"
					y1="0%"
					x2="50%"
					y2="100%"
					stroke="url(#line-grad)"
					stroke-width="10%"
					stroke-linecap="round"
				/>
			</svg>

			Единая система мониторинга и управления качеством питания
		</a>
		<a
			href="/social-map"
			class="btn btn-primary btn-xs mb-3 d-flex gap-2 align-items-center justify-content-center"
		>
			<HomeIcon />
			Социальная карта
		</a>

		<div class="d-flex flex-column mt-auto gap-4">
			<button
				class="btn btn-outline-primary d-flex gap-2 align-items-center justify-content-center"
			>
				<NotificationIcon />

				Уведомления</button
			>

			<div
				class="d-flex flex-row gap-3 justify-content-center align-items-center"
			>
				<img
					src="https://randomuser.me/api/portraits/women/0.jpg"
					alt="User Avatar"
					class="user-avatar"
				/>
				<div>
					<div class="d-flex fw-semibold fs-6 text-nowrap">
						Имя пользователя
					</div>
					<a href="/logout" class="logout-link">Выход</a>
				</div>
			</div>
		</div>
	</div>

	<!-- Main content -->
	<div class="container-fluid d-flex flex-column gap-4 p-5 overflow-auto">
		<slot />
	</div>
</div>

<style>
	.user-avatar {
		width: 50px;
		height: 50px;
		border-radius: 50%;
		margin-right: 10px;
	}
	.user-info {
		display: flex;
		align-items: center;
		margin-bottom: 10px;
	}
	.user-name {
		font-weight: bold;
	}
	.logout-link {
		font-size: 0.8rem;
		color: #6c757d;
		text-decoration: none;
	}
	.notifications-btn {
		position: fixed;
		bottom: 20px;
		left: 20px;
	}
</style>
