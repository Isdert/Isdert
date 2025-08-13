- Hi, I’m @Isdert
- I'm a linux lover but I'm always too lazy to solve problems

<!---
Isdert/Isdert is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!---
#ifdef GL_FRAGMENT_PRECISION_HIGH

precision highp float;

#else

precision mediump float;

#endif

uniform float time;

uniform int pointerCount;

uniform vec3 pointers[10];

uniform vec2 resolution;

void main(void) {

	float mx = max(resolution.x, resolution.y);	vec2 uv = gl_FragCoord.xy / mx;

	vec3 color = vec3(

		uv,

		0.25 + 0.5 * sin(time));

	for (int n = 0; n < pointerCount; ++n) {

		vec3 hole = vec3(sin(1.5 - distance(

			uv,

			pointers[n].xy / mx) * 8.0));

		color = mix(color, hole, -0.5);

	}
--->

