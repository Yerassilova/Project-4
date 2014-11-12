            var curLoc = 0;
			var score = 0;	
			var inventory = "";
						
		    var hasVisitedRoom0 = false;
		    var hasVisitedRoom1 = false;
		    var hasVisitedRoom2 = false;
		    var hasVisitedRoom3 = false;
		    var hasVisitedRoom4 = false;
			var hasVisitedRoom5 = false;
			var hasVisitedRoom6 = false;
			var hasVisitedRoom7 = false;
			var hasVisitedRoom8 = false;
			var hasVisitedRoom9 = false;
			var hasVisitedRoom10 = false;
			
		   //initial function
		   function init() {
		        updateDisplay();
				buttonVisibility();			
			    document.getElementById("picture").style.visibility = "hidden";
				takeButtonVisibility();
				document.getElementById("mainText").readOnly = true;
				document.getElementById("scoreText").readOnly = true;
				} 
			   
		   //navigation functions
		    function btn_go_North() {
		    if (curLoc === 3) {
			    curLoc = 0;	
                updateDisplay();			
			   } else {
			       if (curLoc === 0) {
				       curLoc = 1;	
                       updateDisplay();					   
			        } else {
					    if (curLoc === 4) {
				            curLoc = 5;	
                             updateDisplay();
						 } else {
							  if (curLoc === 5) {
				                  curLoc = 6;	
                                  updateDisplay();
							    } else {
					                if (curLoc === 8) {
				                        curLoc = 7;	
                                        updateDisplay();
						              } else {
							               if (curLoc === 10) {
				                               curLoc = 8;	
                                               updateDisplay();
							                 } else {
					                             navigationError();
											}
										}
									}
					             }		
					        }
					  }
					buttonVisibility();
			     } 

		    function btn_go_South() {
			    if (curLoc === 1) {
			        curLoc = 0;	
                    updateDisplay();
			     } else {
			          if (curLoc === 0) {
				          curLoc = 3;
                          updateDisplay();				  
				     } else {
					     if (curLoc === 6) {
				             curLoc = 5;	
                             updateDisplay();
						 } else {
							  if (curLoc === 5) {
				                  curLoc = 4;	
                                  updateDisplay();
							    } else {
					                if (curLoc === 7) {
				                        curLoc = 8;	
                                        updateDisplay();
						              } else {
							               if (curLoc === 8) {
				                               curLoc = 10;	
                                               updateDisplay();
							                  } else {
					                             navigationError();
											}
										}
									}
					             }		
					        }
					    }	
                     buttonVisibility();						
		           }
		    
		    function btn_go_West() {
		      if (curLoc === 4) {
                  curLoc = 0;  
                  updateDisplay();		  
			      } else {
			           if (curLoc === 0) {
				           curLoc = 2;	
                           updateDisplay();					   
				        } else {
						    if (curLoc === 7) {
				                curLoc = 6;	
                                updateDisplay();
						    } else {
							    if (curLoc === 6) {
				                    curLoc = 1;	
                                    updateDisplay();
							     } else {
							          if (curLoc === 8) {
				                          curLoc = 5;	
                                          updateDisplay();
							           } else {
					                        if (curLoc === 10) {
				                                curLoc = 4;	
                                                updateDisplay();
						                     } else {
							                      if (curLoc === 9) {
				                                      curLoc = 8;	
                                                      updateDisplay();
							                       } else {
					                                     navigationError();
													}
												}
										    }
									  }
								 }
						   }
					            		
				    }
                  buttonVisibility();					
		      }			 
			         
		    function btn_go_East(){
		     if (curLoc === 2) {
			     curLoc = 0;
                 updateDisplay();				 
			     } else {
			          if (curLoc === 0) {
			              curLoc = 4;
                          updateDisplay();		          
			            } else {
						      if (curLoc === 1) {
				                  curLoc = 6;	
                                  updateDisplay();
							  } else {
							       if (curLoc === 6) {
				                       curLoc = 7;	
                                       updateDisplay();
									} else {
							            if (curLoc === 5) {
				                            curLoc = 8;	
                                            updateDisplay();
									    } else {
							                if (curLoc === 4) {
				                                curLoc = 10;	
                                                updateDisplay();
									         } else {
							                     if (curLoc === 8) {
				                                     curLoc = 9;	
                                                     updateDisplay();
									              } else {
					                                  navigationError();
												}
											}
										}
								   }
					          }					  
					     }
		            }
                  buttonVisibility();					
		        }

            function txtCommand_keypress(e) {
				 if (e.which === 13) {
				     document.getElementById("go").onclick();
					 }
			}
		
			function btnGo_click() {             			
               txtCommand.value = txtCommand.value.toLowerCase();				  
			    if (txtCommand.value === "north" || txtCommand.value === "n") {				
			        btn_go_North();					
			       } else {
			           if (txtCommand.value === "south" || txtCommand.value === "s") {
				           btn_go_South();
				         } else {
					         if (txtCommand.value === "east" || txtCommand.value === "e") {
						         btn_go_East();
					           } else {
						           if (txtCommand.value === "west" || txtCommand.value === "w") {
							           btn_go_West();
							         } else {
							             if (txtCommand.value === "take" || txtCommand.value === "t") {
							                 btn_take();
							             } else {
							                 unknownCommand();
											}
										}
						             }
					            }
			               }
		            }
		  
		  //story functions
		    function updateDisplay(message) {
		             checkScore();
		             dspScore();		            
                     switch(curLoc) {
                        case 0: room0();
                                break;
                        case 1: room1();
                                break;
                        case 2: room2();
                                break;
                        case 3: room3();
                                break;
                        case 4: room4();
                                break;
						case 5: room5();
						        break;
						case 6: room6();
						        break;
						case 7: room7();
						        break;
						case 8: room8();
						        break;
						case 9: room9();
						        break;
					   case 10: room10();
                                break;					  
                        default: message = "You cannot go this way.";
                    }	
		  }
		  		 
            function room0() {
		     message = "You are standing inside a mansion's hall. In the mansion" + 
			           " there is a canary in a cage covered with black cloth, so" + 
					   " that it does not sing and you cannot hear it. Your aim is" + 
					   " to find the bird and release it. If it sings when flies" + 
					   " away, you will become the happiest person."; //room 0
			 presentMessage(message);	
		  }
		  
		    function room1() {
		     message = "You entered a dark room with no windows, so you cannot see"+ 
			           " anything..."; //room 1
			 presentMessage(message);
		  }
		 
		    function room2() {
		     message = "You entered a living room, there is a table and an armchair"+ 
			           " in front of a chimney."; //room 2
			 presentMessage(message);
		  }
		  
		    function room3() {
			   if ( inventory.indexOf("map") >= 0) {
			       message = "You are in a big room, there is a grand piano in the" +
			                 " middle of the room and nothing else."; //room 3
				} else {	
                   message = "You are in a big room, there is a grand piano in the" +
			                 " middle of the room. There is a map on the piano," + 
							 " you should take it!"; //room 3
		        }
		        presentMessage(message);
			}
	  
		    function room4() {			     
			   if ( inventory.indexOf("flashlight") >= 0) {
		            message = "You have entered a kitchen."; //room 4			        
				} else {
				   message = "You have entered a kitchen. You can see" + 
				             " a flashlight on a table. The falshlight" + 
							 " will help you to enter the dark room and" + 
							 " see what's there."; //room 4				     
		        }
			    presentMessage(message);
		    }
		  
		    function room5() {
		     message = "This is a dining hall. There is a large round table" + 
			           " in the middle of the room."; //room 5
			 presentMessage(message);
		  }
		  
		    function room6() {
		      if ( inventory.indexOf("Music") >= 0) {
		            message = "You entered a small and narrow corridor. You can" + 
			                  " see pictures of previous owners of the mansion"; //room 6		        
				} else {
				   message = "You entered a small and narrow corridor. You can" +  
			                  " see pictures of previous owners of the mansion" + 
							  " and a music sheet that is lying on the floor." + 
							  " You can take it, it might become useful..."; //room 6				     
		        }
			    presentMessage(message);
		    }
		  
		  
		    function room7() {
		     message = "Now you are in a bedroom. There is a" + "\n" + 
			           "bad, a desk and an old mirror in the room." + "\n" + 
					   "Now you need to look at the mirror..."; //room 7
			 presentMessage(message);
		  }
		  
		    function room8() {
		     message = "room 8"; //room 8
			 presentMessage(message);
		  }
		  
		    function room9() {
		     message = "room 9"; //room 9
			 presentMessage(message);
		  }
		  
		    function room10() {
		     message = "room 10"; //room 10
			 presentMessage(message);
		  }
		  		  		  
		    function navigationError() {		          
			  presentMessage("You cannot go that way.");		     		 		        
		   }
		   
		    function unknownCommand() {
		      presentMessage("I don't understand your command.");
		   }
	   		
	    
			function btn_take() {
				if (curLoc === 3 && inventory.indexOf("map") < 0) {
				    inventory = inventory + " map ";
					document.getElementById("picture").style.visibility = "visible";					
					message = "You have taken the map of the mansion.";
                    checkScore();
		            dspScore();	
                    document.getElementById("takeButton").disabled = true;					
				 } else {			 
			        if (curLoc === 4 && inventory.indexOf("flashlight") < 0) {
				        inventory = inventory  + " flashlight ";
					    message = "You have taken a flashlight.";	
                        checkScore();
		                dspScore();	
                        document.getElementById("takeButton").disabled = true;	
                      } else {
                          if (curLoc === 6 && inventory.indexOf("Music") < 0) {
				              inventory = inventory + " Music Sheet ";									
					          message = "You have taken Music Sheet.";
                              checkScore();							  
		                      dspScore();	
                              document.getElementById("takeButton").disabled = true;						 
			                } else {
					             message = "There is nothing to take in this room.";
						 } 
					 }
			    }
			  presentMessage(message);
			}
				  		
	       /*
		   function items() {
		     var item1 = new map();
			 var item2 = new flashlight();
		   }
		   
		   function map() {
		     this.contents = "map";
		   } 
		   
		    function flashlight() {
		      this.contents = "flashlight";
			  
			}
		   */
		   
		    function showInventory() {	      
			   message = "Your inventory includes:" + " " + inventory;
			   presentMessage(message);			  
		   }

		   function btn_Help() {
		        message = "Navigate with buttons north, south, east, or west." + 
				          " Collect items available with by pressing Take button" + 
						  " or typing take into the command text area. Check your" + 
						  " inventory by pressing My Inventory button. Score is" + 
						  " reflected on the right. To see the map, you have to find it";
				presentMessage(message);
		   }
		   
		  //utility functions
		   function presentMessage(message) {
			   var target = document.getElementById("mainText");
               target.value = message + "\n\n" + target.value;
            }	
			
			function takeButtonVisibility() {
			    if (curLoc === 3) {
				     if (inventory.indexOf("map") < 0) {
				         document.getElementById("takeButton").disabled = false;
				    } else {
				         document.getElementById("takeButton").disabled = true;
				    }
				
				} else {
					if (curLoc === 4) {
					   if (inventory.indexOf("flashlight") < 0){				        
						   document.getElementById("takeButton").disabled = false;
						} else {
				             document.getElementById("takeButton").disabled = true;
				        }
					    
				} else { 
                     if (curLoc === 6) {
					     if (inventory.indexOf("Mus") < 0){				        
						     document.getElementById("takeButton").disabled = false;
					      } else { 
                              document.getElementById("takeButton").disabled = true;
                            }									                                							  
				} else {
				      document.getElementById("takeButton").disabled = true;
					 }
				   }
                }
            }			
				   

		   function buttonVisibility() {
		     switch(curLoc) {
			    case 0: document.getElementById("northBtn").disabled = false;
			            document.getElementById("southBtn").disabled = false;
			            document.getElementById("westBtn").disabled = false;
			            document.getElementById("eastBtn").disabled = false;
				        document.getElementById("takeButton").disabled = true;
                        break;						
				case 1: document.getElementById("northBtn").disabled = true;
				        document.getElementById("westBtn").disabled = true;
                        document.getElementById("takeButton").disabled = true;						
						break;
				case 2: document.getElementById("northBtn").disabled = true;
			            document.getElementById("southBtn").disabled = true;
			            document.getElementById("westBtn").disabled = true;
						document.getElementById("eastBtn").disabled = false;
						document.getElementById("takeButton").disabled = true;
						break;
				case 3: document.getElementById("southBtn").disabled = true;
			            document.getElementById("westBtn").disabled = true;
			            document.getElementById("eastBtn").disabled = true;
						document.getElementById("northBtn").disabled = false;
						takeButtonVisibility();
						break;
				case 4: document.getElementById("southBtn").disabled = true;
				        document.getElementById("eastBtn").disabled = false;
						document.getElementById("westBtn").disabled = false;
						document.getElementById("northBtn").disabled = false;
						takeButtonVisibility();
						break;
				case 5: document.getElementById("westBtn").disabled = true;
			            document.getElementById("eastBtn").disabled = false;
						document.getElementById("northBtn").disabled = false;
			            document.getElementById("southBtn").disabled = false;
						document.getElementById("takeButton").disabled = true;
						break;
				case 6: document.getElementById("northBtn").disabled = true;
				        document.getElementById("southBtn").disabled = false;
			            document.getElementById("westBtn").disabled = false;
			            document.getElementById("eastBtn").disabled = false;
                        takeButtonVisibility();						
				        break;
				case 7: document.getElementById("northBtn").disabled = true;
			            document.getElementById("southBtn").disabled = false;
						document.getElementById("eastBtn").disabled = true;
						document.getElementById("westBtn").disabled = false;
						document.getElementById("takeButton").disabled = true;
						break;
				case 8: document.getElementById("northBtn").disabled = false;
			            document.getElementById("southBtn").disabled = false;
						document.getElementById("eastBtn").disabled = false;
						document.getElementById("westBtn").disabled = false;
						document.getElementById("takeButton").disabled = true;
						break;
				case 9: document.getElementById("northBtn").disabled = true;
			            document.getElementById("southBtn").disabled = true;
						document.getElementById("eastBtn").disabled = true;
						document.getElementById("westBtn").disabled = false;
						document.getElementById("takeButton").disabled = true;
						break;
			   case 10: document.getElementById("northBtn").disabled = false;
			            document.getElementById("southBtn").disabled = true;
						document.getElementById("eastBtn").disabled = true;
						document.getElementById("westBtn").disabled = false;
						document.getElementById("takeButton").disabled = true;
						break;
			   default: document.getElementById("northBtn").disabled = false;
			            document.getElementById("southBtn").disabled = false;
			            document.getElementById("westBtn").disabled = false;
			            document.getElementById("eastBtn").disabled = false; 
						document.getElementById("takeButton").disabled = true;
		     }
		   }
			
		  // functions for keeping and showing score!
		   function checkScore() {
		     if (curLoc === 0) {
		         if (! hasVisitedRoom0) {	        
			         score = score + 5;
				     hasVisitedRoom0 = true;
				 }
		     }
		     
		    if (curLoc === 1) {			
			      if (! hasVisitedRoom1) {			  
			          score = score + 5;
				      hasVisitedRoom1 = true;
				  }
			 }
				 							 		
			if (curLoc === 2) {
			     if (! hasVisitedRoom2) {
			         score = score + 5;
				     hasVisitedRoom2 = true;
				  }
			 }
				   			   
			if (curLoc === 3) {
				  if (! hasVisitedRoom3) {
			          score = score + 5;
				      hasVisitedRoom3 = true;
			       }
			 }
				 
			if (curLoc === 4) {
			    if (! hasVisitedRoom4) {
			        score = score + 5;
				    hasVisitedRoom4 = true;				 
			     }
			 }
				 
			if (curLoc === 5) {
			    if (! hasVisitedRoom5) {
			        score = score + 5;
				    hasVisitedRoom5 = true;				 
			     }
			 }
				 
			if (curLoc === 6) {
			    if (! hasVisitedRoom6) {
			        score = score + 5;
				    hasVisitedRoom6 = true;				 
			     }
			 }
				 
			if (curLoc === 7) {
			    if (! hasVisitedRoom7) {
			        score = score + 5;
				    hasVisitedRoom7 = true;				 
			     }				 
			 }
			 
			 if (curLoc === 8) {
			    if (! hasVisitedRoom8) {
			        score = score + 5;
				    hasVisitedRoom8 = true;				 
			     }
			 }
			 
			 if (curLoc === 9) {
			    if (! hasVisitedRoom9) {
			        score = score + 5;
				    hasVisitedRoom9 = true;				 
			     }
			 }
			 
			 if (curLoc === 10) {
			    if (! hasVisitedRoom10) {
			        score = score + 5;
				    hasVisitedRoom10 = true;				 
			     }
			 }
	 
			 if (curLoc === 3 && inventory.indexOf("map") >= 0) {
			     score = score + 5;
			 }
			 
			 if (curLoc === 4 && inventory.indexOf("flashlight") >= 0) {
			     score = score + 5;
				}
			
			if (curLoc === 6 && inventory.indexOf("Music") >= 0) {
			     score = score + 5;
				}
			 
		 }     			
		  function dspScore() {			         
			     document.getElementById("scoreText").value = "Score:" + score;
		 }
