<script setup>
import Title from './Title.vue';
</script>

<template>
        <Title title="Memberships" />
    <div class="memberships-cont">
        <n-card content-style="padding: 0;" class="accordion">
            <n-tabs type="line" size="large" :tabs-padding="20" pane-style="padding: 20px;">
                <n-tab-pane name="CREW MEMBER">
                    <div class="card1-img">
                        <div class="card-cont">
                            <span class="member-title">CREW MEMBER</span>
                            <p class="member-desc">As a crew member, you'll have access to our club facilities and be able
                                to
                                participate in club events and activities. This membership level is designed for those who
                                are
                                just starting out in the world of sailing and want to learn and develop their skills.</p>

                            <h4>Benefits:</h4>
                            <ul>
                                <li>Access to the club facilities</li>
                                <li>club events and activities</li>
                                <li>sailing lessons and workshops</li>
                                <li>Access junior lever yachts</li>
                                <li>discounts on club merchandise and events</li>
                            </ul>
                            <div class="numbers-cont">
                                <div>
                                    <h1>20+</h1>
                                    <span>yacths</span>
                                </div>
                                <div>
                                    <h1>10+</h1>
                                    <span>courses</span>
                                </div>
                                <div>
                                    <h1>100+</h1>
                                    <span>members</span>
                                </div>
                            </div>
                            <n-space>
                                <n-button type="info">
                                    Purchase membership
                                </n-button>
                            </n-space>
                        </div>
                    </div>

                </n-tab-pane>
                <n-tab-pane name="CRUISE MEMBER">
                    <div class="card2-img">
                        <div class="card-cont">
                            <span class="member-title">CRUISE MEMBER</span>
                            <p class="member-desc">As a cruise member, you'll have all the benefits of a crew member, plus
                                additional perks that are designed for those who want to explore the waterways and coastal
                                areas near our club.</p>

                            <h4>Benefits:</h4>
                            <ul>
                                <li>All the benefits of a crew member</li>
                                <li>discounted rates for boat rentals and charters</li>
                                <li>access to navigational resources</li>
                                <li>Access to mid lever yachts</li>
                                <li>invitations to exclusive club cruises and events</li>
                            </ul>
                            <div class="numbers-cont">
                                <div>
                                    <h1>20+</h1>
                                    <span>yacths</span>
                                </div>
                                <div>
                                    <h1>10+</h1>
                                    <span>courses</span>
                                </div>
                                <div>
                                    <h1>100+</h1>
                                    <span>members</span>
                                </div>
                            </div>

                        </div>
                    </div>
                </n-tab-pane>
                <n-tab-pane name="HONORARY MEMBER">
                    <div class="card3-img">
                        <div class="card-cont">
                            <span class="member-title">HONORARY MEMBER</span>
                            <p class="member-desc">As an honor member, you'll have access to the highest level of benefits
                                and privileges that our club has to offer. This membership level is designed for those who
                                are passionate about sailing and want to immerse themselves in the yacht club experience.
                            </p>

                            <h4>Benefits:</h4>
                            <ul>
                                <li>All the benefits of a cruise member</li>
                                <li>Access to exclusive member-only events</li>
                                <li>Priority registration for club activities and events</li>
                                <li>Access to the club's private dining room</li>
                                <li>Access to senior lever yachts</li>
                            </ul>
                            <div class="numbers-cont">
                                <div>
                                    <h1>20+</h1>
                                    <span>yacths</span>
                                </div>
                                <div>
                                    <h1>10+</h1>
                                    <span>courses</span>
                                </div>
                                <div>
                                    <h1>100+</h1>
                                    <span>members</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </n-tab-pane>
            </n-tabs>
        </n-card>
    </div>
</template>

<style scoped>
.memberships-cont {
    width: 100%;
    display: flex;
    justify-content: center;
   
}

.numbers-cont {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}

.member-title {
    font-size: 30px;
    font-weight: bold;
}

.member-desc {
    text-shadow: 1px 1px 1px black;
}

.card-cont {
    width: 40%;
    height: fit-content;
    margin-right: 10%;
    color: white;
    text-shadow: 1px 1px 1px black;
}

.card1-img {
    background-image: url('../assets/images/crew-y1.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    height: 70vh;
    display: flex;
    justify-content: flex-end;
    align-items: center;
}

.card2-img {
    background-image: url('../assets/images/cruise-y1.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    height: 70vh;
    display: flex;
    justify-content: flex-end;
    align-items: center;
}

.card3-img {
    background-image: url('../assets/images/honor-y1.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    height: 70vh;
    display: flex;
    justify-content: flex-end;
    align-items: center;
}

.memberships-cont .n-card {
    width: 100%;
}

.accordion {
    width: min-content;
}

.card-img {
    width: 100%;
}
</style>
