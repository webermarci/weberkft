<script lang="ts">
</script>

<section id="contact" class="bg-zinc-50 p-5 md:p-8">
	<div class="mx-auto grid max-w-6xl gap-10 lg:grid-cols-5 lg:items-start">
		<div class="col-span-2 flex flex-col gap-3">
			<p class="text-sm font-medium tracking-widest text-primary uppercase">Kapcsolat</p>
			<div class="space-y-4">
				<h2 id="contact-title" class="roboto-slab text-4xl font-bold">
					Beszéljünk a következő digitális lépésről.
				</h2>
				<p class="max-w-xl text-muted-foreground">
					Írd meg röviden, miben segíthetünk, és hamarosan felvesszük veled a kapcsolatot.
				</p>
			</div>
		</div>

		<form class="card form col-span-3 gap-5 p-6 shadow-xs" aria-label="Kapcsolatfelvételi űrlap">
			<div class="grid gap-5 md:grid-cols-2">
				<div class="field">
					<label for="contact-name">
						Név<span class="text-primary" aria-hidden="true">*</span>
					</label>
					<input id="contact-name" name="name" type="text" autocomplete="name" required />
				</div>

				<div class="field">
					<label for="contact-email">
						Email<span class="text-primary" aria-hidden="true">*</span>
					</label>
					<input id="contact-email" name="email" type="email" autocomplete="email" required />
				</div>
			</div>

			<div class="field">
				<label for="contact-company">Cég</label>
				<input id="contact-company" name="company" type="text" autocomplete="organization" />
			</div>

			<div class="field">
				<label for="contact-message">
					Miben segíthetünk?<span class="text-primary" aria-hidden="true">*</span>
				</label>
				<textarea id="contact-message" name="message" required></textarea>
			</div>

			<div class="flex flex-col gap-4 pt-2 md:flex-row md:items-center md:justify-between">
				<p class="text-sm text-muted-foreground">
					<span class="text-primary" aria-hidden="true">*</span> Kötelező mezők
				</p>
				<button type="submit" class="btn-primary">Üzenet küldése</button>
			</div>
		</form>
	</div>
</section>
