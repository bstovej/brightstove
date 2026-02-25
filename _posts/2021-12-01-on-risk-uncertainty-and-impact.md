---
layout: post
title: "On risk, uncertainty, and impact"
date: 2021-12-01 14:01:12
categories: [Awareness, Risk Management]
tags: [risk decision, threat, uncertainty, vulnerability]
---

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">Risk management is an approach that is commonly used across many industries. However, the language of risk has not been consistent or easy to understand across existing risk literatures. In particular, the definition of risk is at times mixed with uncertainty (e.g., ISO 31000 and ISO/IEC 73), and described in terms of the value of the asset involved (e.g., ISO 51 and 63). This has not helped in evaluating, and making risk informed decisions. This blog is an attempt to clarify and provide better understanding of these terminologies.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size"><strong>Risk versus Uncertainty</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">Risk and uncertainty are two separate concepts or ideas. Risk is neither a subset nor a branch of uncertainty principles. As Frank Knight pronounced in his classic work “Risk, uncertainty, and profit”, “If you don’t know for sure what will happen, but you know the odds, that’s risk, and if you don’t even know the odds, that’s uncertainty”(Knight, 2006). This delineation of risk and uncertainty is fundamental and important.</p>
<!-- /wp:paragraph -->

<!-- wp:quote {"className":"is-style-plain","fontSize":"small"} -->
<blockquote class="wp-block-quote is-style-plain has-small-font-size"><p>Risk is tied to the possibility of loss, like gambling. Uncertainty, on the other hand, is merely the unknown; loss is not always involved. Yet, uncertainty makes us more uneasy than when we face a situation that has known risks. … The uncertainty we face in the dark has no real risk, just perceived risk, because we do not know, for sure, what’s out there. We desire an order, or perfect knowledge, that comes only when we turn on the lights. In the dark, there is no order&nbsp;(Bernstein, 1999).</p></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">As noted above, uncertainty is not necessarily a bad thing. Recognizing uncertainty is part of the decision-making process.</p>
<!-- /wp:paragraph -->

<!-- wp:quote {"className":"is-style-plain","fontSize":"small"} -->
<blockquote class="wp-block-quote is-style-plain has-small-font-size"><p>We experience true uncertainty when we do not know the probabilities of the possible outcomes because we do not even know what all of the possible outcomes are. By understanding how truly ignorant we are, we will be able to make better decisions, even as we continue to make mistakes&nbsp;(Peter Edgar in Bernstein, 1999, p. x).</p></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size"><strong>On Risk&nbsp;</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">Quantitatively, risk is normally expressed in terms of a probability of occurrence of the threats involved. This probability number is influenced by the presence of vulnerability, and the ease of exploitation of the vulnerability.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">The constituent parts of a risk are therefore the threats and vulnerabilities associated with the system being evaluated. In other words, risk is a function of threats and vulnerabilities, or <em>r = f (t x v) (McChrystal &amp; Butrico, 2021, pp. 10-11; <em> Stewart, Chapple, &amp; Gibson, 2015, p. 62</em>)</em>. Risk exists when there is a threat in or around the system, and the system has vulnerability (or weakness) that can be exploited by the threat. When the exploitation takes place, the risk is realized, or materialized. If a threat has a high probability of occurrence, but the associated vulnerability cannot be easily exploited, then the risk is effectively low. The converse is also true. We can also say that if there is no threat, i.e., <em>r = f (0, v) = 0</em>, there is no risk. Similarly, when there is no vulnerability, i.e., <em>r = f (t, 0) = 0</em>, there is also no risk. There will however always be threats (either introduced by human being, technology, or nature, e.g., hurricane, earthquake), and weaknesses will always exist in any given system. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">In the context of digital information systems, when managing information security risks, we use threat hunting, threat intelligence, and threat detection systems to help identify, detect, and measure threats that are operating or emerging in and around our system, and we use tools such as vulnerability scanning, penetration testing, and patch management systems to identify, detect, and update/patch our systems vulnerabilities. By detecting threats early, and being prepared for their occurrence, we can isolate, block, and/or contain the blast radius (or scope of effect) of the threat thereby reducing risk to our system. Similarly, by getting our systems updated to the latest patch available, or implement workarounds to reduce exploitability of a vulnerability, we reduce our risk exposure level.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">Note that there may also be other factors that can influence risk. For example, time, as in Winn Schwartau’s “Time-based Security”&nbsp;(Schwartau, 2001). In the equity market, the timeliness of information plays a significant role in preventing frauds such as insider trading and ensuring fair market practices. In such a situation, risk of unauthorized disclosure of information that have influence over a company’s stock price changes with time. Before the information goes public (e.g., announcement of a strategic acquisition or merger), the risk of unauthorized disclosure will be closely watched. But once the information has been released to the public, it is no longer confidential, but the integrity will remain important. Risk of unauthorized modification will continue to be an important focus.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size"><strong>Risk versus impact (or Consequences)</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">The probability of a risk materializing, as computed from the risk equation (where r = f (t, v)), should not be confused with the potential magnitude of impact that the risk may cause. For example, a statement such as, “the risk is high as it can cause significant financial losses to our organization” is misleading. Does the risk have a high probability of occurrence because of the financial value involved, or because there is a threat that is likely to materialize due to the existence of certain vulnerabilities that can be easily exploited? We need clarity in order to manage the risk effectively. The magnitude of a risk materializing, also known as potential impact, is the outcome or consequence, not inherent in the risk itself. Impact is related to the value of the system as an asset, not the risk per se. Impact assessment is therefore a separate tool that is used in risk management, not in risk analysis. We should not rate a risk as high simply because the value of the asset involved is high.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">By separating impact from the risk measurement, we can make our risk management decisions based on the significance of the risk in relation to the value of assets independently. We can weigh which is more important in a given context, and whether to focus on the value of the asset, or the risk specifically. Considering a two-level high-low risk rating system, we will have four situations:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true,"type":"1","fontSize":"small"} -->
<ol type="1" class="has-small-font-size"><li>Low risk, high impact</li><li>Low risk, low impact</li><li>High risk, low impact&nbsp;</li><li>High risk, high impact</li></ol>
<!-- /wp:list -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">It is clear from this breakdown that our top priority for managing risk will be on systems that fall into situation #4--high risk, high impact. Our next priority, i.e., either #1 or #3, will depend on whether we consider the principle of "security is only as strong as the weakest link" should weigh more than the value of the specific asset involved.&nbsp;&nbsp;In a highly connected system environment where low and high value assets are interconnected and have dependency on each other, a high-risk issue despite being found on a low value asset may still result in impacting high value asset due to their dependency and/or connectivity. In such a case, situation #3 will take precedence over situation #1. Alternatively, we may isolate systems in #3 and address the risk issue in situation #1 with a higher priority.&nbsp;&nbsp;In either case, addressing situation #1 will still be desired to prevent or reduce the effect of a Black Swan event (Taleb, 2007) should the low risk materialize on a high value system. We should also continue to monitor and re-evaluate systems in situation #2 to make sure that they neither become the "weakest link" nor a Black Swan.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size"><strong>References</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">Bernstein, P. L. (1999).&nbsp;<em>Patterns in the Dark - Understanding risk and financial crisis with complexity theory</em>: John Wiley &amp; Sons, Inc.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">Knight, F. (2006).&nbsp;<em>Risk, uncertainty and profit</em>. New York: Dover Publications, Inc.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">McChrystal, S., &amp; Butrico, A. (2021).&nbsp;<em>Risk - A User’s Guide</em>: Penguin Business.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">Schwartau, W. (2001).&nbsp;<em>Time Based Security - Measuring Security and Defensive Strategies in a Networked Environment</em>&nbsp;(Revised ed.): Interpact Press.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">Stewart, J. M., Chapple, M., &amp; Gibson, D. (2015).&nbsp;<em>(ISC)2 Certified Information Systems Security Professional (CISSP) Official Study Guide</em>&nbsp;(7th ed.): John Wiley and Sons.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"small"} -->
<p class="has-small-font-size">Taleb, N. N. (2007).&nbsp;<em>The Black Swan</em>: Pengiun Books.</p>
<!-- /wp:paragraph -->