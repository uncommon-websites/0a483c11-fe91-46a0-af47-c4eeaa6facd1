<script>
	let openIndex = 0;
	const faqs = [
		{
			question: "What industries does AVIVYS specialize in?",
			answer: "AVIVYS specializes in technology and financial services recruitment. We have deep expertise in placing talent for banks, fintech companies, technology firms, and consulting organizations across global markets."
		},
		{
			question: "Do you handle international placements?",
			answer: "Yes! We operate across 40+ countries and have extensive experience with cross-border hiring, compliance requirements, and international talent acquisition strategies."
		},
		{
			question: "What types of roles can AVIVYS help fill?",
			answer: "We handle both contract and permanent placements across technology (software engineering, cloud, data, security) and financial services (banking, trading, risk management, compliance) at all levels from individual contributors to executive leadership."
		},
		{
			question: "How does AVIVYS use AI in recruitment?",
			answer: "We use AI and machine learning to enhance sourcing, screening, and candidate matching at scale. However, every placement is managed by experienced consultants who ensure quality, cultural fit, and domain expertise."
		},
		{
			question: "What is your typical time-to-hire?",
			answer: "Time-to-hire varies by role complexity and location, but our AI-enabled process and global network typically allow us to present qualified candidates within 1-2 weeks and complete placements within 4-8 weeks."
		},
		{
			question: "What engagement models do you offer?",
			answer: "We offer flexible engagement models including project-based recruitment, retained search, embedded talent partnerships, and ongoing recruitment programs tailored to your specific needs and hiring volume."
		}
	];
</script>

<section class="py-24">
	<div class="mx-auto max-w-[1400px] px-6">
		<div class="grid grid-cols-1 gap-16 lg:grid-cols-12">
			<!-- Left Side -->
			<div class="lg:col-span-4">
				<div class="mb-4 text-[10px] font-bold tracking-widest text-gray-500 uppercase">[06] FAQ</div>
				<h2 class="mb-6 text-4xl font-medium tracking-tight text-gray-900">Your questions, answered</h2>
				<p class="mb-8 text-lg leading-relaxed text-gray-600">
					Have more questions? Our team is ready to discuss your specific hiring needs and how AVIVYS can help you achieve better outcomes.
				</p>
				<a href="#" class="inline-block bg-gray-900 px-6 py-3 text-[11px] font-bold tracking-widest text-white transition-colors hover:bg-gray-800 uppercase">
					Contact Us
				</a>
			</div>

			<!-- Right Side (Accordion) -->
			<div class="lg:col-span-8">
				<div class="divide-y divide-gray-200 border-t border-b border-gray-200">
					{#each faqs as faq, i}
						<div class="group">
							<button 
								class="flex w-full items-center justify-between py-6 text-left focus:outline-none"
								onclick={() => openIndex = openIndex === i ? -1 : i}
							>
								<span class="text-lg font-medium text-gray-900">{faq.question}</span>
								<span class="ml-4 flex h-6 w-6 items-center justify-center text-gray-400">
									{#if openIndex === i}
										<svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M18 6L6 18M6 6l12 12"/></svg>
									{:else}
										<svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 5v14M5 12h14"/></svg>
									{/if}
								</span>
							</button>
							{#if openIndex === i}
								<div class="pb-6 text-gray-600 leading-relaxed">
									{faq.answer}
								</div>
							{/if}
						</div>
					{/each}
				</div>
			</div>
		</div>
	</div>
</section>