<template>
	<section class="getTicketSection" id="getTicketSection">
		<div class="proofMainContainer getTicketContainer">
			<h1>SECURE YOUR TICKET:</h1>
			<div class="row justify-content-between getTicketcards">
				<div class="col-md-6 col-sm-12 mb-4 px-lg-4">
					<div class="ticketCard generalPass text-center">
						<div>
							<span>{{ tickets[0].type }}</span>
							<h2>{{ tickets[0].price }}</h2>
							<h3>{{ tickets[0].price_subtext }}</h3>
							<p>
								{{ tickets[0].features }}
							</p>
						</div>
						<a :href="tickets[0].buy_ticket_link" target="_parent">
							<button>GET TICKETS</button>
						</a>
					</div>
				</div>
				<div class="col-md-6 col-sm-12 mb-4 px-lg-4">
					<div class="ticketCard vipPass text-center">
						<div>
							<span>{{ tickets[1].type }}</span>
							<h2>{{ tickets[1].price }}</h2>
							<h3>{{ tickets[1].price_subtext }}</h3>
							<p>
								{{ tickets[1].features }}
							</p>
						</div>

<div id="eventbrite-widget-container-901458806557"></div>

<script src="https://www.eventbrite.com/static/widgets/eb_widgets.js"></script>

<script type="text/javascript">
    var exampleCallback = function() {
        console.log('Order complete!');
    };

    window.EBWidgets.createWidget({
        // Required
        widgetType: 'checkout',
        eventId: '901458806557',
        iframeContainerId: 'eventbrite-widget-container-901458806557',

        // Optional
        iframeContainerHeight: 425,  // Widget height in pixels. Defaults to a minimum of 425px if not provided
        onOrderComplete: exampleCallback  // Method called when an order has successfully completed
    });
</script>

						<a :href="tickets[1].buy_ticket_link" target="_parent">
							<button>GET TICKETS</button>
						</a>
					</div>
				</div>
			</div>
						<a
				href="https://app.eukapay.com/templates/tmp_AjlmxqkN19bHy4hE7gNZsBtH2I"
				class="buyWithCyrpto"
				target="_blank"
			>
				<button> BUY WITH CRYPTO</button>
			</a>
		</div>
	</section>

</template>
<script>
import ticketsConfig from "@/config/2024/tickets.json";
export default {
	data() {
		return {
			tickets: ticketsConfig.data,
		};
	},
};
</script>
