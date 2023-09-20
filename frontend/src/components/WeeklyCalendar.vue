<template>
    <div class="calendar">
        <div class="times">
            <div class="spacer"></div>
            <div class="specific-time">8 AM</div>
            <div class="specific-time">9 AM</div>
            <div class="specific-time">10 AM</div>
            <div class="specific-time">11 AM</div>
            <div class="specific-time">12 PM</div>
            <div class="specific-time">1 PM</div>
            <div class="specific-time">2 PM</div>
            <div class="specific-time">3 PM</div>
            <div class="specific-time">4 PM</div>
            <div class="specific-time">5 PM</div>
            <div class="specific-time">6 PM</div>
            <div class="specific-time">7 PM</div>
            <div class="specific-time">8 PM</div>
        </div>
        <div class="days-of-the-week">
            <div class="monday">
                <div class="date">
                    <p class="date-num">1</p>
                    <p class="date-day">Monday</p>
                </div>
            </div>
            <div class="tuesday">
                <div class="date">
                    <p class="date-num">2</p>
                    <p class="date-day">Tuesday</p>
                </div>
            </div>
            <div class="wednesday">
                <div class="date">
                    <p class="date-num">3</p>
                    <p class="date-day">Wednesday</p>
                </div>
            </div>
            <div class="thursday">
                <div class="date">
                    <p class="date-num">4</p>
                    <p class="date-day">Thursday</p>
                </div>
            </div>
            <div class="friday">
                <div class="date">
                    <p class="date-num">5</p>
                    <p class="date-day">Friday</p>
                </div>
            </div> 
        </div>
    </div>
</template>

<script>
    export default {};
</script>

<style>
/* Styling goes here */
    :root {
    --numDays: 5;
    --numHours: 10;
    --timeHeight: 60px;
    --calBgColor: #fff1f8;
    }

    .calendar {
        display: grid;
        gap: 10px;
        grid-template-columns: auto 1fr;
        margin: 2rem;
    }

    .times {
        display: grid;
        grid-template-rows: repeat(var(--numHours), var(--timeHeight));
    }

    .days-of-the-week {
        display: grid;
        grid-column: 2;
        gap: 5px;
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    }

    .date {
        display: flex;
        gap: 1em;
    }

    .date-num {
        font-size: 3rem;
        font-weight: 600;
        display: inline;
    }

    .date-day {
        display: inline;
        font-size: 3rem;
        font-weight: 100;
    }
</style>