Cleanflight CLI variables related to navigation features

| `Variable`                      | Description/Units                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Min    | Max    |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|--------|
| `align_mag`                        | When using an external magnetometer sensor this should be set to actual sensor alignment relative to board. Values: DEFAULT, CW0, CW90, CW180, CW270, CW0FLIP, CW90FLIP, CW180FLIP, CW270FLIP | | |
| `gps_provider`                     | GPS hardware type: NMEA, UBLOX, I2C | | |
| `failsafe_procedure`               | Failsafe type: SET-THR - set throttle to `failsafe_throttle`, RTH - execute RTH sequence if possible, land otherwise | | |
| `inav_accz_unarmedcal`             | Controls if inertial position estimator should compute gravity offset on accelerometer Z-axis dynamically when drone is unarmed. Mostly affects accuracy of altitude estimation and althold performace. No real reason to disable this feature. | OFF | ON |
| `inav_dead_reckoning`              | | OFF | ON |
| `inav_gps_delay`                   | GPS position and velocity data usually arrive with a delay. This parameter defines this delay. Default should be reasonable for most GPS receivers. | 0 | 500 |
| `inav_w_z_baro_p`                  | | 0 | 10 |
| `inav_w_z_gps_p`                   | | 0 | 10 |
| `inav_w_z_gps_v`                   | | 0 | 10 |
| `inav_w_xy_gps_p`                  | | 0 | 10 |
| `inav_w_xy_gps_v`                  | | 0 | 10 |
| `inav_w_xy_dr_v`                   | | 0 | 10 |
| `inav_w_z_res_v`                   | | 0 | 10 |
| `inav_w_xy_res_v`                  | | 0 | 10 |
| `inav_w_acc_bias`                  | | 0 | 1 |
| `inav_max_eph_epv`                 | | 0 | 9999 |
| `inav_baro_epv`                    | | 0 | 9999 |
| `nav_alt_p`                        | | | |
| `nav_alt_i`                        | | | |
| `nav_alt_d`                        | | | |
| `nav_vel_p`                        | | | |
| `nav_vel_i`                        | | | |
| `nav_vel_d`                        | | | |
| `nav_pos_p`                        | | | |
| `nav_pos_i`                        | | | |
| `nav_pos_d`                        | | | |
| `nav_posr_p`                       | | | |
| `nav_posr_i`                       | | | |
| `nav_posr_d`                       | | | |
| `nav_navr_p`                       | | | |
| `nav_navr_i`                       | | | |
| `nav_navr_d`                       | | | |
| `nav_use_midrc_for_althold`        | | OFF | ON |
| `nav_throttle_tilt_comp`           | | OFF | ON |
| `nav_user_control_mode`            | Defines how Pitch/Roll input from RC receiver affects flight in POSHOLD mode: ATTI - right stick controls attitude like in ANGLE mode; CRUISE - right stick controls velocity in forward and right direction. | | |
| `nav_dterm_cut_hz`                 | | 0 | 100 |
| `nav_wp_radius`                    | Waypoint radius. Waypoint would be considered reached if machine is within this radius | 100 | 2000 |
| `nav_max_speed`                    | Maximum velocity firmware is allowed in full auto modes (POSHOLD, RTH, WP)  | 10 | 2000 |
| `nav_manual_speed`                 | Maximum velocity firmware is allowed when processing pilot input for POSHOLD/CRUISE control mode | | |
| `nav_manual_climb_rate`            | Maximum climb/descent rate firmware is allowed when processing pilot input for ALTHOLD control mode | | |
| `nav_min_rth_distance`             | | | |
| `nav_rth_alt_mode`                 | Altitude control mode: CURRENT, EXTRA, FIXED, MAX, AT_LEAST | | |
| `nav_rth_altitude`                 | | | |
| `nav_mc_hover_thr`                 | Multicopter hover throttle hint for altitude controller. Should be set to approximate throttle value when drone is hovering. | 1000 | 2000 |
| `nav_fw_cruise_thr`                | | | |
| `nav_fw_min_thr`                   | | | |
| `nav_fw_max_thr`                   | | | |
| `nav_fw_bank_angle`                | | | |
| `nav_fw_climb_angle`               | | | |
| `nav_fw_dive_angle`                | | | |
| `nav_fw_pitch2thr`                 | | | |
| `gyro_soft_filter`                 | | | |
| `acc_soft_filter`                  | | | |
| `baro_tab_size`                    | | | |
| `baro_noise_lpf`                   | | | |
| `magzero_x`                        | | | |
| `magzero_y`                        | | | |
| `magzero_z`                        | | | |
| `acczero_x`                        | | | |
| `acczero_y`                        | | | |
| `acczero_z`                        | | | |
| `accgain_x`                        | | | |
| `accgain_y`                        | | | |
| `accgain_z`                        | | | |