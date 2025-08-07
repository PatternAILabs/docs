<style>
.md-main__inner, .md-content {
  max-width: 100% !important;
  width: 100% !important;
  padding: 0 !important;
}

.full-width-container {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  align-items: center;
  margin-bottom: 2rem;
}

.md-card {
  display: block;
  width: 100%;
  max-width: 530px;
  text-decoration: none;
  color: inherit;
  border-radius: 0.5rem;
  overflow: hidden;
  box-shadow: var(--md-shadow-z2);
  flex-shrink: 0;
}

.overlay-card {
  position: relative;
  width: 100%;
  padding-top: 56.25%; 
  overflow: hidden;
  background-color: #000;
}

.overlay-card img {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  object-fit: cover;
  opacity: 0.8;
}

.overlay-card-text h3 {
  margin: 0 0 0.5rem;
}

.overlay-card-text p {
  margin: 0;
  font-size: 0.95rem;
}

.full-width-container > div {
  flex: 1;
  min-width: 300px;
}
</style>
#
<!-- Agent Build -->
<div class="full-width-container">
  <a href="http://localhost:8001/prerequisites/" class="md-card">
    <article class="overlay-card">
      <img src="/images/build.jpeg" alt="AgentBuild">
    </article>
  </a>
  <div>
    <h2 style="font-weight: 810; font-size: 36px; margin-top: -30px;">Agent Build</h2>
    <p style="text-align: justify !important;">
      PatternAI Agent is a modular voice AI framework that powers natural conversations using speech and text. It supports plug-and-play STT, TTS, and LLM services with real-time monitoring via Langfuse. Built for flexibility—perfect for tasks like shopping, travel, and beyond.
    </p>
  </div>
</div>

<!-- Agent Test -->
<div class="full-width-container" style="flex-direction: row-reverse;">
  <a href="http://localhost:8002/setup/" class="md-card">
    <article class="overlay-card">
      <img src="/images/test.png" alt="AgentTest">
    </article>
  </a>
  <div>
    <h2 style="font-weight: 810; font-size: 36px; margin-top: -10px; text-align: right;">Agent Test</h2>
    <p style="text-align: justify !important;">
      AgentTest is an automated QA pipeline for conversational AI that generates tests, evaluates responses, and visualizes performance—all from a single prompt. It scores your agent across language quality, factual accuracy, and task fulfillment using LLMs and Langfuse. No manual testing, just instant insight. Build smarter, iterate faster.
    </p>
  </div>
</div>
